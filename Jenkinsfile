pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Alfiya-git/Alfiya.git'
            }
        }

        stage('Deploy Docker Container') {
            steps {
                script {
                     sh "docker run -itd -p 80:80 stacksimplify/kube-nginxapp1:1.0.0"

                    }
                }
            }
        }
    }
