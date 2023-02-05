pipeline {
    agent any

    stages{
        stage('Clone repository"'){
            steps{
               git url: 'https://github.com/pradyumna93/awesome-repo.git'
            }
        }
        stage('Build Docker Image'){
            steps {
                sh "docker build -t pradyumna93/Djano_App:1.0"
            }
    }
    
}
}