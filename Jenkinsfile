pipeline {
    agent any

    stages {
        stage('Clone  Repository') {
            steps {
                git 'https://github.com/satyaprakash196/Python-Flask.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('flask-ci-cd-app')
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                     docker.image('flask-ci-cd-app').run('-p 5000:5000')
                }
            }
        }
    }
}
