pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'dockerhub-cred') {
                        sh 'docker build -t gsaiadhinathareddy/shippingservice:v1 .'
                    }
                }
            }
        }
        stage('Push') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'dockerhub-cred') {
                        sh 'docker push gsaiadhinathareddy/shippingservice:v1'
                    }
                }
            }
        }
    }
}
