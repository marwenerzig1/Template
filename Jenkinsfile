pipeline {
    agent any

    tools {
      gradle 'Gradle'      
    }
    
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn ...'
                nodejs('Node-10.17'){
                     sh 'yarn install'
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
