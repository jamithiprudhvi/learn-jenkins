pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment { 
        GREETINGS = 'Hello Jenkins'
    }
    options {
        timeout(time: 1, unit: 'SECONDS') 
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
                sh """
                    echo "Here i wrote shell script"
                    echo "$GREETINGS"
                    sleep 10
                """
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