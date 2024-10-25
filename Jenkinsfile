pipeline {
    agent any  

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    bat "docker build -t xacuti01/dock ."
                }
            }
        }
        stage('Build and Run Docker Container') {
            steps {
                script {
                    bat "docker rm -f 2347 || exit 0"
                    bat "docker run -d --name 2347 xacuti01/dock"
                }
            }
        }
    }
}

