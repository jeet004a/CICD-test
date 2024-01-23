pipeline {
        agent {
        docker { image 'python:3' }
    }
        stages { 
            stage('Build') {
                steps {
                    echo 'Start building'
                }
            }
            stage('Test') {
                steps {
                    sh 'pip --version'
                }
            }
            stage('Deploy') {
                steps {
                    echo 'complete deploy'
                }
            }
        }
    }
