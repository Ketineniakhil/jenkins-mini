pipeline {
    agent { 
        docker { 
            image 'node:23.8.0' 
        } 
    }
    stages {
        stage('Build') {
            steps {
                sh 'node --version'
                echo "Build stage"
            }
        }
        stage('Test') {
            steps {
                echo "Test stage"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration Test stage"
            }
        }
    } 
}
