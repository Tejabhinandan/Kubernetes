pipeline {
    agent any

    environment {
        KUBECONFIG = "/home/ubuntu/.kube/config"
    }

    stages {

        stage('Deploy') {
            steps {
                sh 'kubectl apply -f pod.yaml'
            }
        }

        stage('Verify') {
            steps {
                sh 'kubectl get pods -o wide'
            }
        }
    }
}
