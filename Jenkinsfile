pipeline {
    agent any
    environment {
        PYTHON_VERSION = '3.8'
    }
    stages {
        stage('Setup') {
            steps {
                script {
                    sh 'export PATH=$PATH:/path/to/python' + env.PYTHON_VERSION + '/bin'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'python3 manage.py migrate'
                }
            }
        }
    }
}
