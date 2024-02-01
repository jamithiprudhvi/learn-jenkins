pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    // Build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    // post Build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'This runs when pipeline is failed, used generally to send some alerts'
        }
        success { 
            echo 'It will say hello when pipe line is success'
        }
    }
}