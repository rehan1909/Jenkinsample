pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Explicitly checkout your Git repository from GitHub
                git url: 'https://github.com/rehan1909/Jenkinsample.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                // For demonstration, display the content of app.py
                sh 'cat app.py'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run the Python script to simulate testing (ensure python3 is installed)
                sh 'python3 app.py'
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
