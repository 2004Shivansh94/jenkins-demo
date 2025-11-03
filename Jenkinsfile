pipeline {
    agent any

    tools {
        maven 'Maven'   // Make sure Maven is configured in Jenkins under Manage Jenkins > Global Tool Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning code from GitHub...'
                git branch: 'main', url: 'https://github.com/2004Shivansh94/jenkins-demo.git'
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling Java code...'
                bat 'mvn compile'
            }
        }

        stage('Build/Package') {
            steps {
                echo 'Building and packaging the project...'
                bat 'mvn clean package'
            }
        }

        stage('Unit Testing') {
            steps {
                echo 'Running unit tests...'
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to server (simulated)...'
                bat 'echo Deployment successful!'
            }
        }
    }
}
