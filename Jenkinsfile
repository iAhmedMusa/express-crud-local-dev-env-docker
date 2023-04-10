pipeline {
	agent { label 'docker-agent-alpine' }

	environment {
		DOCKERHUB_CREDENTIALS=credentials('docker_hub_creds')
	}
    stages {
      stage("build") {
        steps {
              echo 'Building the app...'
              sh 'docker --version'
              // sh 'docker build -t ahmedmusa/express-crud-mongo:latest ./app'
        }
      }

      stage("test") {
        steps {
              echo 'testing the app...'
        }
      }

      stage("deploy") {
        steps {
              echo 'deploying the app...'
        }
      }

    }
  }
