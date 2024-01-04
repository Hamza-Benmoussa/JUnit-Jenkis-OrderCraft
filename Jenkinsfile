pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'java8'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Mouslih0/JUnit-Jenkis-OrderCraft/'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }

        failure {
             echo 'Build failed!'
        }
    }
}