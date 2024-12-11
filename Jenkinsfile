pipeline {
    agent any

    environment {
        PROJECT_NAME = "MyProject"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your_username/your_repository.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    echo "Building the project..."
                    sh 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Running tests..."
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deploying the project..."
                    sh './deploy.sh'
                }
            }
        }

        stage('Cleanup') {
            steps {
                script {
                    echo "Cleaning up..."
                    sh 'mvn clean'
                }
            }
        }
    }

    post {
        success {
            echo "Build and tests passed successfully!"
        }
        failure {
            echo "Build or tests failed. Please check the logs."
        }
        always {
            echo "This block will always run regardless of the result."
        }
    }
}
 
