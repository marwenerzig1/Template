pipeline {
    agent any
    stages {
        stage('go to folder ') {
            steps {
                cd d:
                cd D:\Project Devops\tt
            }
         }
         stage('verify docker version ') {
            steps {
                echo 'dockerr versionn '
                bat "docker --version"
            }
         }
         stage('lunsh docker compose for create the containers') {
            steps {
                bat 'docker-compose docker-compose.yaml up'
            }
         }
         stage('go to the url') {
            steps {
                bat 'start localhost:8070'
            }
         }
    }
}
