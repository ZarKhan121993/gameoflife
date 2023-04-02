pipeline{
    agent{
        label "slave1"
    }

    stages{
        stage('build'){
            steps{
                sh "rm -rf /mnt/slave1/workspace/job1"
                sh "sudo mvn install"
            }
        }
         stage('docker'){
            steps{
                sh "sudo docker run -itdp 8080:8080 -v --name tomact tomcat"
            }
        }
    }

}
