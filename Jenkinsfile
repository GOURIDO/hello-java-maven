pipeline {
    agent any
    tools {
        maven 'Maven 3.8.7'  // Use the version of Maven installed in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/GOURIDO/hello-java-maven.git'  // Your GitHub repo URL
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}
