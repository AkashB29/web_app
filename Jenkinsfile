pipeline{
    agent any
    stages{
        stage('Clone Repository'){
            steps{
                git branch: 'main', url: 'https://github.com/AkashB29/web_app.git'
            }
        }
        stage('Build Docker Image'){
            steps{
                bat 'docker build -t web_app .'
            }
        }stage('Run Docker Container'){
            steps{
                bat 'docker run -d -p 8081:80 web_app:latest'
            }
        }
            
    }
}