pipeline {
    agent any
    environment {
        MAVEN_HOME = "/usr/share/maven"
        PATH = "$MAVEN_HOME/bin:$PATH"
    }
    stages {
        stage('Verify Tools') {
            steps {
                sh 'java -version'
                sh 'mvn --version'
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
    }
}
