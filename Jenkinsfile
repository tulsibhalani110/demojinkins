pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'gradle:8.2.0-jdk17-alpine'
                }
            }
            steps {
                sh 'gradle --version'
            }
        }
    }
}
