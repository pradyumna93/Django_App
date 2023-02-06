pipeline {
    agent any
       docker { 
            image 'docker:19.03.12'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }

    stages{
        stage('Clone repository"'){
            steps{
               git url: 'https://github.com/pradyumna93/awesome-repo.git'
            }
        }
        stage("Build Dockerfile") {
            steps {
                sh 'docker build -t Django_App:$BUILD_NUMBER .'  
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
