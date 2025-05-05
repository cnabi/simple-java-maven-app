pipeline {
    agent any
    tools {
        maven 'Maven 3'
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
