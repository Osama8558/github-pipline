pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t osama-cicd-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f osama-cicd-container || true'
                sh 'docker run -d --name osama-cicd-container -p 8088:80 osama-cicd-app'
            }
        }
    }
}
