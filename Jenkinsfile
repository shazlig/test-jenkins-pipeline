pipeline {
    stages {
        stage('Deploy Patient App') {
            steps {
                withCredentials([
                    string(credentialsId: 'minikube', variable: 'api_token')
                    ]) {
                    sh 'kubectl --token $api_token --server https://44.229.31.144:8443 --insecure-skip-tls-verify=true apply -f some.yaml '
                }
            }
        }
    }
}
