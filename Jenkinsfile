pipeline {
    agent any
	 environment {
        DJANGO_SETTINGS_MODULE = 'polling.settings'
        VIRTUAL_ENV = 'venv'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'export PATH=$PATH:/path/to/python3/bin'
                }
            }
        }
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
		stage('Run Tests') {
            steps {
                script {
                    sh "source $VIRTUAL_ENV/bin/activate && python manage.py test"
                }
            }
        }
		stage('Deploy') {
            steps {
                script {
                    echo 'this is deploye block'
                }
            }
        }
		
    }
}
