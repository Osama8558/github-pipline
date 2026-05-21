pipeline {
    agent any

    stages {
        stage('Stop Old Container') {
            steps {
                sh 'docker stop osama-app || true'
                sh 'docker rm osama-app || true'
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t osama8558/devops-auto-app:latest .'
            }
        }

        stage('Push Image to Docker Hub') {
            steps {
                sh 'docker push osama8558/devops-auto-app:latest'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8090:80 --name osama-app osama8558/devops-auto-app:latest'
            }
        }
    }
}
