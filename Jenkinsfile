pipeline {
    agent any
	 environment {
        DJANGO_SETTINGS_MODULE = 'polling.settings'
        VIRTUAL_ENV = 'venv'
	PYTHON3_PATH = '/path/to/python3/bin'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh "export PATH=${env.PYTHON3_PATH}:${env.PATH}"
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
