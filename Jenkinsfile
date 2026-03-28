pipeline {
    agent any

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
