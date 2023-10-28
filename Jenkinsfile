
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.12.0-alpine3.18' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh '''
                      git clone https://github.com/sameeriron42/two-way-integration.git
                        cd two-way-integration
                        pip install -r requirements.txt
                        export PYTHONPATH="${PYTHONPATH}:./app"
                '''
            }
        }
    }
}

