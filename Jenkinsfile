pipeline {
    agent any   // use your agent

    stages {
        stage('Clone Code') {
            steps {
                echo "Cloning repo..."
                git 'https://github.com/Tejabhinandan/Kubernetes.git'
            }
        }

        stage('Check Files') {
            steps {
                sh 'ls -l'
            }
        }

        stage('Deploy Pod') {
            steps {
                sh 'kubectl apply -f pod.yaml'
            }
        }
    }
}
