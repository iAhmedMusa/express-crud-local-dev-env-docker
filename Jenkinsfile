pipeline{

	agent any

	environment {
		DOCKERHUB_CREDENTIALS=credentials('Docker_hub_creds')
	}

	stages {

		stage('Build') {

			steps {
				sh 'docker build -t ahmedmusa/express-crud-mongo:latest ./app'
			}
		}

		stage('Login') {

			steps {
				sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
			}
		}

		stage('Push') {

			steps {
				sh 'docker push ahmedmusa/express-crud-mongo:latest'
			}
		}
	}

	post {
		always {
			sh 'docker logout'
		}
	}

}