pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/2004Shivansh94/jenkins-demo'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
