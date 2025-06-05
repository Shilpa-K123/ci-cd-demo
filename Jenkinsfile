pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Shilpa-K123/ci-cd-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sample-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name sample-app sample-app || echo "Container might already be running"'
            }
        }
    }
}

