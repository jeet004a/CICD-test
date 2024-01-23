pipeline {
        agent any
        stages { 
            stage('Build') {
                steps {
                    echo 'Start building'
                    sh 'pip --version'
                    sh 'python -m pip install -r requirements.txt'
                }
            }

            stage('Test') {
                steps {
                    sh 'python polling/manage.py test ./polling'
                }
            }

            stage('Deploy') {
                steps {
                    sh 'echo not yet...'
                }
            }
        }
    }
