pipeline {
    agent any
    tools {
        maven 'Maven 3.8.7'  // Make sure this matches the installed Maven version in Jenkins
    }
    environment {
        GITHUB_TOKEN = credentials('github-token')  // Optional if you need token authentication
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/GOURIDO/hello-java-maven.git', credentialsId: 'your-credentials-id'  // Use proper credentials if needed
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
                sh 'mvn deploy -DaltDeploymentRepository=github-repository::default::https://maven.pkg.github.com/GOURIDO/hello-java-maven'
            }
        }
    }
}

