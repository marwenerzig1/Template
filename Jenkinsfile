pipeline {
    agent any

    tools {
      gradle 'Gradle-8.2.1'   
      nodejs 'Node-10.17'
    }
    
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn ...'
                echo 'just for test ...'
                sh "npm install -g yarn"
                sh "yarn install"
            }
        }
        stage('run backend') {
            steps {
                echo 'executing nodejs ...'
                sh 'gradle -version'
            }
        }
    }
}
