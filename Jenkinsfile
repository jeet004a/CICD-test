pipeline {
    agent any
	 environment {
        DJANGO_SETTINGS_MODULE = 'polling.settings'
        VIRTUAL_ENV = 'jack'
	PYTHON3_PATH = '/path/to/python3/bin'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'export PATH=$PATH:/path/to/python3/bin'
		    sh '/path/to/python3/bin/python3 -m venv $VIRTUAL_ENV'
                    sh "source $VIRTUAL_ENV/bin/activate && pip install -r requirements.txt"
		    sh "source $VIRTUAL_ENV/bin/activate && python manage.py test"
                }
            }
        }
		stage('Deploy') {
            steps {
                script {
                    echo 'this is deploy block'
                }
            }
        }
		
    }
}
