pipeline {
    agent any
    stages {
        stage('verify tooling') {
            steps {
                echo 'dockerr infoooo '
                sh 'docker info' 
                echo 'dockerr versionn '
                sh 'docker version'
                echo 'dockerr composeee '
                sh 'docker compose version'
                echo 'curl version  '
                sh 'curl --version'
                echo 'jq version'
                sh 'jq --version'
            }
        }
    }
}
