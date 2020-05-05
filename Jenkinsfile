pipeline {
    agent any
     environment {
         KUBECONFIG = '/home/.kube/config'
     }
    stages {
        stage('Build') {
            steps {
                sh 'docker-compose build'
            }
        }
        stage('Deploy to K8s Cluster') {
            steps {
                sh 'kubectl apply -f kube-deployment.yml'
            }
        }
    }
}
