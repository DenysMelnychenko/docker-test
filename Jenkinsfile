pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Замість "docker.build" використовуйте підхід через sh або bat команди
                    sh 'docker build -t my-angular-app .'
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
                    // Для push імеджу використовуйте команду через sh
                    sh 'docker push my-angular-app:latest'
                }
            }
        }
    }
}
