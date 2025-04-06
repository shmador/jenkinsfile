pipeline {
    agent any
    environment {
	SNYK_TOKEN = cardentials('snyk-token')
    }
	
    stages {
        stage('Build') {
            steps {
		script {
			sh 'docker build -t web .'
		}
            }
        }

        stage('Test') {
            steps {
            	echo 'test'
		snykSecurity {
			snykInstallation: 'snyk@latest'
			snykTokenId: SNYK_TOKEN 
		}  
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}
