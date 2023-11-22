pipeline {
    agent none
    stages {
        stage('Back-end') {
            agent {
                docker { image 'maven:3.9.5-eclipse-temurin-17-alpine' }
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'node:20.9.0-alpine3.18' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}
