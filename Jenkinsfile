pipeline {
    environment {
        DOCKER_HOST = ''
        DOCKER_TLS_VERIFY = ''
    }
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 9000:9000'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
            }
        }
    }
}