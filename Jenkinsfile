pipeline {
    agent {
        label {
                label "built-in"
                customWorkspace "/mnt/pipeline"
        }
    }
    stages {
        stage ("Master") {
            steps {
                sh "rm -rf *"
                sh 'yum install git -y'
            }
        }
        stage ("Slave-1") {
            agent {
                label {
                    label 'MG'
                    customWorkspace "/mnt/pipeline-2"
                }
            }
            steps {
                sh "rm -rf *"
                sh "sudo yum install git -y"
            }
            
        }
    }
}
