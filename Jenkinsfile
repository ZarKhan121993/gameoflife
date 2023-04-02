pipeline{
    agent{
        label{
            label "label1"
            customWorkspace "/mnt/slave1/project"
        }
    }
    stages{
        stage('build){
            steps{
                sh "mvn clean install"
            }
        }
    }

}
