pipeline{
    agent{
        label{
             label "slave1"
             customWorkspace "/mnt/data"
        }  
    }

    stages{
        stage('build'){
            steps{
                    sh "rm -rf *"
                    sh "mvn install"
            }
        }
         stage('docker'){
            steps{
                sh "yum install docker -y"
                sh "service docker start"
                sh "docker run -itdp 8080:8080 -v --name tomact tomcat"
            }
        }
    }

}
