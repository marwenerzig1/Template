pipeline {
    agent any
    stages {
        stage('verify docker version ') {
            steps {
                echo 'dockerr versionn '
                bat "docker --version"
            }
         }
        stage('go to folder ') {
            steps {
                cd tt
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
