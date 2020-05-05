pipeline {
    agent any
     environment {
         KUBECONFIG = '/home/.kube/config'
     }
    stages {
        stage('Build') {
            steps {
                sh 'cat ~/my_password.txt | docker login --username varunlokeswaran --password-stdin'
                sh 'docker-compose build'
                sh 'docker-compose push'
            }
        }
        stage('Deploy to K8s Cluster') {
            steps {
                sh 'kubectl apply -f kube-deployment.yml'
            }
        }
    }
}
