pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                git 'https://github.com/AdeshAJ/Jenkins-Pipeline-for-CI-CD.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker image...'
                script {
                    docker.build('simpleapp:latest')
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "No tests implemented yet."'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying container...'
                sh 'docker run -d -p 3000:3000 simpleapp:latest'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
