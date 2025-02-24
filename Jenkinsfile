pipeline {
    agent any
    environment{
        dockerHome = tool 'myDocker'
        mavenHome = tool 'myMaven'
        PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
                sh 'docker --version'
                echo "Build stage"
            }
        }
        stage('Test') {
            steps {
                echo "Test-stage"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration Test stage"
            }
        }
    } 
}
