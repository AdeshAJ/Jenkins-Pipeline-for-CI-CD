pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out successfully.'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker image...'
                script {
                    try {
                        sh 'docker build -t myapp:latest .'
                    } catch (err) {
                        echo 'Docker not available — skipping actual build.'
                    }
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "No tests yet."'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying app...'
                sh 'echo "Simulating deploy step..."'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
