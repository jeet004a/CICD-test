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
                    sh 'virtualenv venv && . venv/bin/activate && pip install -r requirements.txt && python tests.py'
                }
            }
            stage('Deploy') {
                steps {
                    echo 'complete deploy'
                }
            }
        }
    }
