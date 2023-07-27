pipeline{

	agent {label 'linux'}

	environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub-acces')
	}

	stages {
	    
	    stage('gitclone') {

			steps {
				git 'https://github.com/marwenerzig1/Template.git'
			}
		}

		stage('Build') {

			steps {
				bat 'docker build -t marwenerzig1/nodeapp_test:latest .'
			}
		}

		stage('Login') {

			steps {
				bat "echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin"
			}
		}

		stage('Push') {

			steps {
				bat "docker push marwenerzig1/nodeapp_test:latest"
			}
		}
	}

	post {
		always {
			bat "docker logout"
		}
	}

}
