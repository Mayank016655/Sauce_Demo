pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'JDK11'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Mayank016655/Sauce_Demo.git'
            }
        }
        stage('Build & Test') {
            steps {
                bat 'mvn clean test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}