pipeline {
    agent any
    tools {
        maven 'Maven 3.9.6'  // Ensure this matches what's configured in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/cnabi/simple-java-maven-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
