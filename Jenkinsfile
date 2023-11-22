pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    def customImage = docker.build('tulsibhalani110/alpine:latest', '.')
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

