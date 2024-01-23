pipeline {
        agent any
        stages { 
            stage('Build') {
                steps {
                    echo 'Start building'
                }
            }
            stage('Test') {
                steps {
                    python3 -m venv env
                }
            }
            stage('Deploy') {
                steps {
                    echo 'complete deploy'
                }
            }
        }
    }
