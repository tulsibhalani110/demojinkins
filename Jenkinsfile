pipeline {
    agent any

    stages {
        stage('Pull Docker Image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials-id') {
                        // Pull the Alpine Linux image
                        def alpineImage = docker.image('alpine:latest')
                        alpineImage.pull()
                    }
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

