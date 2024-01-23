pipeline {
        agent any
        environment {
        DJANGO_SETTINGS_MODULE = 'polling.settings'
        VIRTUAL_ENV = 'venv'
    }
        stages { 
                stage('Checkout') {
                    steps {
                        checkout scm
                 }
            }
                stage('Install Dependencies') {
            steps {
                script {
                    sh 'python3 -m venv $VIRTUAL_ENV'
                    sh "source $VIRTUAL_ENV/bin/activate && pip install -r requirements.txt"
                }
            }
        }
            
        }
    }
