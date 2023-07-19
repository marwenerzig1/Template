pipeline {
    agent any
    stages {
        stage('verify docker info ') {
            steps {
                echo 'dockerr infoooo '
                sh 'docker info' 
            }
         }
        stage('verify docker version ') {
            steps {
                echo 'dockerr versionn '
                sh 'docker version'
            }
         }
        stage('verify docker compose ') {
            steps {
                echo 'dockerr composeee '
                sh 'docker compose version'
            }
         }
         stage('verify curl ') {
            steps {
                echo 'curl version'
                sh 'curl --version'
            }
         }
        stage('verify jq ') {
            steps {
                echo 'jq version'
                sh 'jq --version'
            }
         }
    }
}
