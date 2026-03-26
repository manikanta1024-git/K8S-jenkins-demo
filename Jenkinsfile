pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t your-image:latest .'
            }
        }
        stage('Push') {
            steps {
                sh 'docker push your-registry/your-image:latest'
            }
        }
        stage('Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
            }
        }
    }
}