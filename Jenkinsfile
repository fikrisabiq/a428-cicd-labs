pipeline {
    environment {
        DOCKER_HOST = ''
        DOCKER_TLS_VERIFY = ''
    }
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install --prefer-offline --no-audit --progress=false'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}