pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		sh 'docker build -t web .'
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
