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
			additionalArguments: '--docker web'
			failOnIssues: false
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
