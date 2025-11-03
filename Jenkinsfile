pipeline {
    agent any

    stage('Checkout') {
    steps {
        git branch: 'main', url: 'https://github.com/2004Shivansh94/jenkins-demo.git'
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
