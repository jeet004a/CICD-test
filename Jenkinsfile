pipeline {
        agent any
        stages {
            stage('Build') {
                steps {
                    sh 'pip install -r requirements.txt'
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
