pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'dockerhub-cred') {
                        sh 'docker build -t gsaiadhinathareddy/productcatalogservice:v1 .'
                    }
                }
            }
        }
        stage('Push') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'dockerhub-cred') {
                        sh 'docker push gsaiadhinathareddy/productcatalogservice:v1'
                    }
                }
            }
        }
    }
}
