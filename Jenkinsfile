pipeline{
    agent any
    stages{
        stage('clone repo'){
            steps{
                git branch :'main', url:'https://github.com/PSumaiah/web-dev-app.git'
            }
        }
        stage('build docker images'){
            steps{
            bat 'docker build -t web-dev-app .'
            }
        }
        stage('run docker container'){
            steps{
                bat 'docker run -d -p 8080:80 --name web-container web-dev-app'
            }
        }
    }
}