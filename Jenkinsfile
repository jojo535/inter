pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your code repository if needed
                // For example:
                // git 'https://github.com/your/repository.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                // Build NGINX Docker image
                script {
                    docker.build('my-nginx-image', '-f /path/to/Dockerfile .')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                // Run NGINX Docker container
                script {
                    docker.image('my-nginx-image').run('-p 8080:80 --name my-nginx-container -d')
                }
            }
        }
    }
}
