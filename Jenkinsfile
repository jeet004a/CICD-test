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
                    sh 'virtualenv venv && . venv/bin/activate && pip install -r requirements.txt'
                }
            }

            stage('Deploy') {
                steps {
                    echo 'complete deploy'
                }
            }
        }
    }
