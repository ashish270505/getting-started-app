pipeline {
    agent any

    stages {
        // Step 1: Clone the Git repository
        stage('Get Git Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/ashish270505/getting-started-app.git'
            }
        }

        // Step 2: Build the Docker image
        stage('Build Docker Image') {
            steps {
               

                bat 'docker build -t todo:latest .'
            }
        }

        // Step 3: Save the Docker image locally (for Docker Desktop)
        stage('Push Docker Image') {
            steps {
                bat 'docker run -d todo:latest'
            }
        }
    }
}