pipeline {
    agent any

    tools {
      Gradle 'Gradle'
      NodeJS 'Node-10.17'
      
    }
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn ...'
                sh 'yarn install'
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
