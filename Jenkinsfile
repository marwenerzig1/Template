pipeline {

  agent { dockerfile true }

  environment {
    DOCKERHUB_CREDENTIALS = credentials('marwenerzig1-dockerhub')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t marwenerzig1/mongo:latest .'
      }
    }
    stage('Login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }
    stage('Push') {
      steps {
        sh 'docker push marwenerzig1/mongo:latest'
      }
    }
  }
  post {
    always {
      sh 'docker logout'
    }
  }
}
  
