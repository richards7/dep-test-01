pipeline {
    agent { label 'docker-agent' }

    stages {
        stage('Deploy') {
    steps {
        withKubeConfig([credentialsId: 'minikube-kubeconfig']) {
            script {
    
                sh "kubectl apply -f k8s/deployment.yaml"
                sh "kubectl rollout status deployment/my-app"
            }
        }
    }
}
    }
}
