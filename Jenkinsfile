pipeline {
    agent any
    tools {
        jdk 'JDK17'  // Matches the name from Step 2
    }
    environment {
        JAVA_HOME = "/usr/lib/jvm/temurin-17-jdk"
        PATH = "$JAVA_HOME/bin:$PATH"
    }
    stages {
        stage('Verify Java') {
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
