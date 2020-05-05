pipeline {
    agent any
     environment {
         KUBECONFIG = '/home/vagrant/.kube/config'
     }
    stages {
        stage('Build') {
            steps {
                sh 'cat /home/vagrant/docker_password.txt | docker login --username varunlokeswaran --password-stdin'
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
