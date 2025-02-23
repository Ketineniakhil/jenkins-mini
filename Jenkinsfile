pipeline {
    agent { 
        docker { 
            image 'maven:3.6.3' 
        } 
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version' // Corrected command
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
