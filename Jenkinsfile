pipeline {
    agent any
    environment {
        DOCKER_IMAGE = 'my-angular-app'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    docker.build("$DOCKER_IMAGE")
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Додайте команди для запуску тестів, якщо є
            }
        }
        stage('Deploy') {
            steps {
                script {
                    docker.withRegistry('url', 'credentials-id') {
                        docker.image("$DOCKER_IMAGE").push('latest')
                    }
                }
            }
        }
    }
}
