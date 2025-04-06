pipeline {
    agent any
	
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
		snykSecurity(
			snykInstallation: 'snyk@latest',
			snykTokenId: 'snyk-token',
		)
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}
