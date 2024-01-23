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
                    sh "${env.WORKSPACE}/venv/bin/pip install -r requirements.txt"
                }
            }

            stage('Deploy') {
                steps {
                    echo 'complete deploy'
                }
            }
        }
    }
