pipeline {
    agent any
    stages {
        stage('verify docker version ') {
            steps {
                echo 'dockerr versionn '
                bat "docker --version"
            }
         }
         stage('lunsh docker compose for create the containers') {
            steps {
                bat 'docker pull node:lts'
                bat 'docker run -d -p 8050:8050 mongo-express' 
                bat 'docker ps'
            }
         }
         stage('go to the url') {
            steps {
                bat 'start localhost:8050'
            }
         }
    }
}
