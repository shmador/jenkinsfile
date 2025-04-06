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
             withCredentials([string(credentialsId: 'snyktoken', variable: 'TOKEN')]) {
                    sh 'snyk test'
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
