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

        stage('Clone Code') {
    steps {
        git branch: 'main',
        url: 'https://github.com/Dharti-git/docker-nodejs-cicd.git'
    }
}
    }
}