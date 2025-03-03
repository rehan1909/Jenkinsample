pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }
        stage('List Files') {
            steps {
                sh 'ls -la'
            }
        }
    }
}

