pipeline {
    agent any
    environment {
        PYTHON_VERSION = '3.12.0'  // Specify your Python version
        VENV = 'venv'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Setup') {
            steps {
                script {
                    sh "python${PYTHON_VERSION} -m venv ${VENV}"
                    sh "source ${VENV}/bin/activate"
                    sh 'pip install -r requirements.txt'
                }
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    sh 'python manage.py test'
                }
            }
        }
    }
    post {
        always {
            script {
                sh 'deactivate'
            }
        }
    }
}
