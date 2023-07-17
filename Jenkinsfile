pipeline {
    agent any

    tools {
      gradle 'Gradle-8.2.1'      
    }
    
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn ...'
                nodejs('Node-10.17'){
                     sh "npm install -g yarn"
                     sh "yarn install"
                }
            }
        }
        stage('run backend') {
            steps {
                echo 'executing nodejs ...'
                sh './gradlew -v'
            }
        }
    }
}
