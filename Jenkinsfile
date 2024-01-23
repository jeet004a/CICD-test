pipeline {
        agent any
        stages { 
            stage('Build') {
                steps {
                    echo 'Start building'
                }
            }
            stage('Test') {
                sh 'virtualenv env -p python3.12'
                sh 'source env/bin/activate'
                sh 'env/bin/pip install -r requirements.txt'
                sh 'env/bin/python3.12 manage.py test'
                
            }
            stage('Deploy') {
                steps {
                    echo 'complete deploy'
                }
            }
        }
    }
	
	
	
	
