pipeline{
    agent{
        label{
            label "slave1"
            customWorkspace "/mnt/slave1/project"
        }
    }
    stages{
        stage('build){
            steps{
                sh " mvn clean install"
            }
        }
    }

}
