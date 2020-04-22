pipeline {
    agent any
    environment {
        KUBECONFIG = 'C:/Users/varun.l/.kube/config'
    }
    stages {
        stage('Deliver') {
            steps {
                powershell 'kubectl apply -f kube-deployment.yml'
            }
        }
    }
}
