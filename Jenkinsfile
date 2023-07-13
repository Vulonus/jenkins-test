/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'uvicorn main:app --host 0.0.0.0 --port 80'
                sh 'curl -v http://localhost:80/'
            }
        }
    }
}