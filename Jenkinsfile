pipeline {
    agent any

    environment {
        IMAGE_NAME = "my-app-image"
        IMAGE_TAG = "latest"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("${IMAGE_NAME}:${IMAGE_TAG}", "-f build/Dockerfile .")
                }
            }
        }
    }
}
