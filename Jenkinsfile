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
                     sh "kubectl apply -f /app1"

                    }
                }
            }
        }
    }
