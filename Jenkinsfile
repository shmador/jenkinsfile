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
            	echo 'test'    
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}
