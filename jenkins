pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t prod .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'kubectl apply -f deploy.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }
    }
}
