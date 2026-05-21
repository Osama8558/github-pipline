pipeline {
    agent any

    stages {

        stage('Docker Compose Down') {
            steps {
                sh 'docker compose down || true'
            }
        }

        stage('Docker Compose Build') {
            steps {
                sh 'docker compose build'
            }
        }

        stage('Docker Compose Up') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}
