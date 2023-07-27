pipeline {
    agent any
    stages {
        stage('verify docker info ') {
            steps {
                echo 'dockerr info '
                bat "docker info" 
            }
         }
        stage('verify docker version ') {
            steps {
                echo 'dockerr versionn '
                bat "docker --version"
            }
         }
        stage('verify docker compose ') {
            steps {
                echo 'dockerr composeee '
                bat "docker compose version"
            }
         }
         stage('verify curl ') {
            steps {
                echo 'curl version'
                bat 'curl --version'
            }
         }
    }
}
