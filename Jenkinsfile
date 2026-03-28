pipeline {
    agent { label 'doc' }

    environment {
        KUBECONFIG = "/home/ubuntu/.kube/config"
    }

    stages {

        stage('Clone Repo') {
            steps {
                echo "Cloning repository..."
                git 'https://github.com/Tejabhinandan/Kubernetes.git'
            }
        }

        stage('Verify Files') {
            steps {
                sh 'ls -l'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh '''
                kubectl apply -f pod.yaml
                '''
            }
        }

        stage('Check Pods') {
            steps {
                sh 'kubectl get pods'
            }
        }
    }
}
