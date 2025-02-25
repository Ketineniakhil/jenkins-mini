pipeline {
    agent any
    tools {
        jdk 'jdk17'
        maven 'myMaven'
    }
    environment {
        PATH = "$MAVEN_HOME/bin:$PATH"
    }
    stages {
        stage('Verify Environment') {
            steps {
                sh 'java -version'
                sh 'mvn --version'
                sh 'docker --version || echo "Docker not installed"'
            }
        }
        stage('Checkout') {
            steps {
                echo "Checking out the repository..."
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Integration Test') {
            steps {
                sh 'mvn failsafe:integration-test'
            }
        }
    }
}
