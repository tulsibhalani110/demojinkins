pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build the custom Docker image on top of Alpine
                    def customImage = docker.build('your-docker-hub-username/your-custom-image:latest', '.')
                }
            }
        }

        // Additional stages
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed :('
        }
    }
}

