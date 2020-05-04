pipeline {
    agent any
    // environment {
    //     KUBECONFIG = 'C:/Users/varun.l/.kube/config'
    // }
    stages {
        stage('Build') {
            steps {
                sh 'sudo docker-compose build'
            }
        }
        stage('Deploy to K8s Cluster') {
            steps {
                sh 'sudo kubectl apply -f kube-deployment.yml'
            }
        }
    }
}
