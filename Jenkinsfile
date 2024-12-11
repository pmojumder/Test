pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                checkout scm
            }
        }
        stage('Read Text File') {
            steps {
                script {
                    // Read the content of the text file from the repository
                    def fileContent = readFile('New Text Document.txt')
                    
                    // Print the content to the Jenkins console log
                    echo "Content of the text file: ${fileContent}"
                }
            }
        }
    }
}
