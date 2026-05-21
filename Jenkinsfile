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
                sh 'docker build -t osama-devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8090:80 --name osama-app osama-devops-app'
            }
        }

    }
}
