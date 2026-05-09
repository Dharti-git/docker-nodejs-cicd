pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Dharti-git/docker-nodejs-cicd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker rm -f myapp-container || true'
                sh 'docker run -d -p 3000:3000 --name myapp-container myapp'
            }
        }
    }
}