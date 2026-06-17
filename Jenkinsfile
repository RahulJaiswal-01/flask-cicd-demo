pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/RahulJaiswal-01/flask-cicd-demo.git'
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t flask-app .'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                docker stop flask-app || true
                docker rm flask-app || true

                docker run -d \
                --name flask-app \
                -p 5000:5000 \
                flask-app
                '''
            }
        }
    }
}
