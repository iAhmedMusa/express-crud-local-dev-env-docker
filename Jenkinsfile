pipeline {

	agent any
  
  environment {
		DOCKERHUB_CREDENTIALS=credentials('docker_hub_creds')
	}

  stages {
    stage("build") {
      steps {
            echo 'Building the app...'
            sh 'docker --version'
            sh 'docker build -t ahmedmusa/express-crud-mongo:latest ./app'
      }
    }

    stage('Docker Login') {
      steps {
            sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }

    stage('Docker Push') {
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


} //Pipline end
