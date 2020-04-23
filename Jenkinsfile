pipeline {
    agent any
    environment {
        KUBECONFIG = 'C:/Users/varun.l/.kube/config'
    }
    stages {
        stage('Build') {
            steps {
                powershell 'docker-compose build --no-cache'
            }
        }
        stage('Deply to K8s Cluster') {
            steps {
                powershell 'kubectl apply -f kube-deployment.yml'
            }
        }
    }
}
