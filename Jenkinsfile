pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('myapp-image')
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    docker.image('myapp-image').run('-p 5000:5000')
                }
            }
        }
    }
}
