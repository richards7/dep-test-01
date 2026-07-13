stage('Deploy') {
    steps {
        withKubeConfig([credentialsId: 'minikube-config']) {
            script {
    
                sh "kubectl apply -f k8s/deployment.yaml"
                sh "kubectl rollout status deployment/my-app"
            }
        }
    }
}
