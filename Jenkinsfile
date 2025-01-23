pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/jeneeswari-star/docker-jenkins.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-world-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 3000:3000 hello-world-app'
            }
        }
    }
}
