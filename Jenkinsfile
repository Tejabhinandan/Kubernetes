pipeline {
    agent { label 'doc' }

    environment {
        KUBECONFIG = "/home/ubuntu/.kube/config"
    }

    stages {

        stage('Debug Start') {
            steps {
                echo "Pipeline started..."
            }
        }

        stage('List Files') {
            steps {
                sh 'ls -l'
            }
        }

        stage('Deploy Pod') {
            steps {
                sh 'kubectl apply -f pod.yaml'
            }
        }

        stage('Verify') {
            steps {
                sh 'kubectl get pods'
            }
        }
    }
}
