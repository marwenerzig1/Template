pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  environment {
    DOCKERHUB_CREDENTIALS = credentials('jenkins-dockerhub')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t .'
      }
    }
    stage('Login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }
    stage('Push') {
      steps {
        sh 'docker push marwenerzig1/alpine'
      }
    }
  }
  post {
    always {
      sh 'docker logout'
    }
  }
}
