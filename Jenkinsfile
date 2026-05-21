pipeline {
    agent any

    stages {

        stage('Docker Compose Down') {
            steps {
                sh '/usr/bin/docker-compose down || true'
            }
        }

        stage('Docker Compose Build') {
            steps {
                sh '/usr/bin/docker-compose build'
            }
        }

        stage('Docker Compose Up') {
            steps {
                sh '/usr/bin/docker-compose up -d'
            }
        }

    }
}
