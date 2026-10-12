pipeline {
    agent any
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    // Perintah untuk mem-build Docker image dari Dockerfile
                    bat 'docker build -t my-python-app .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    // Perintah untuk menjalankan container dari image yang baru dibikin
                    bat 'docker run --rm my-python-app'
                }
            }
        }
    }
}