pipeline{
    agent{
        label "slave1"
    }

    stages{
        stage('build'){
            steps{
  
                sh "sudo mvn install"
            }
        }
         stage('docker'){
            steps{
                sh "sudo yum install docker -y"
                sh "sudo docker run -itdp 8080:8080 -v --name tomact tomcat"
            }
        }
    }

}
