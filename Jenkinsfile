pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/jeneeswari-star/docker-jenkins.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
                sh 'npm install --save-dev chai'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-world-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8081:8081 hello-world-app'
            }
        }
    }
}
