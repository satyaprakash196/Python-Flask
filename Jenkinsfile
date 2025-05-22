pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/satyaprakash196/Python-Flask.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t python-flask-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 python-flask-app'
            }
        }
    }
}

