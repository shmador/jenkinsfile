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
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
