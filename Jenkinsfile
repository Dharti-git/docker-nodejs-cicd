pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/Dharti-git/docker-nodejs-cicd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t myapp .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker stop myapp-container || exit 0'
                bat 'docker rm myapp-container || exit 0'
                bat 'docker run -d -p 3000:3000 --name myapp-container myapp'
            }
        }
    }
}