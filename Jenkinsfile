pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Explicit checkout from your GitHub repo on branch 'main'
                git url: 'https://github.com/rehan1909/Jenkinsample.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                // For demonstration, display the contents of app.py
                sh 'cat app.py'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run the Python script inside a container that has Python 3 installed
                script {
                    docker.image('python:3.9-slim').inside {
                        // Ensure the workspace is available and run the Python script
                        sh 'python3 app.py'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Placeholder for deployment commands
                sh 'echo "Deployment steps go here."'
            }
        }
    }
}
