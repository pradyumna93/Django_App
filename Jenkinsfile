pipeline {
    agent any

    stages{
        stage('Clone repository"'){
            steps{
               git url: 'https://github.com/pradyumna93/awesome-repo.git'
            }
        }
        stage("Build Dockerfile") {
            steps {
                script{
                    sh "docker.build -t pradyumna93/Django_App."
                }   
            }
        }
        stage("Push code to Docker Hub") {
            steps {
                sh "docker login -u pradyumna93 -p India#5488"
                sh "docker push pradyumna93/Django_App"
            }
        }
    }
}
