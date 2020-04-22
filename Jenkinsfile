pipeline {
    agent {
        any
        // docker {
        //     image 'node:6-alpine'
        //     //args '-p 3000:3000'
        // }
    }
    environment {
        KUBECONFIG = 'C:/Users/varun.l/.kube/config'
    }
    stages {
        // stage('Build') {
        //     steps {
        //         powershell '$env:KUBECONFIG="C:\Users\varun.l\.kube\config"'
        //     }
        // }
        // stage('Test') {
        //     steps {
        //         sh './jenkins/scripts/test.sh'
        //     }
        // }
        stage('Deliver') {
            steps {
                powershell 'kubectl apply -f kube-deployment.yml'
            }
        }
    }
}