pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Alfiya-git/Alfiya.git'
            }
        }

        stage('kube-deploy') {
            steps {
                script {
                     sh "kubectl apply -f 01-Nginx-App1-Deployment-and-NodePortService.yml"
                     sh "kubectl apply -f 02-App1-Ingress.yml"

                    }
                }
            }
        }
    }
