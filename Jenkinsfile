pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                script {
                    sh 'python3 -m venv venv'
                    sh 'source venv/bin/activate'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'pip install -r requirements.txt'
                    sh 'python3 manage.py migrate'
                    // Add other Django build steps
                }
            }
        }

        // Add more stages as needed
    }
}
