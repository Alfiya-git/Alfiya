pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Alfiya-git/Alfiya.git'
            }
        }

        stage('Deploy Docker Container') {
            steps {
                script {
                     sh "docker run -itd -p 80:8082 stacksimplify/kube-nginxapp1:1.0.0"

                    }
                }
            }
        }
    }
