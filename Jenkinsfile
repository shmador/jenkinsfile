pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		image 'gradle:8.2.0-jdk17-alpine'
		reuseNode true
            }
        }
        stage('Test') {
            steps {
                sh 'gradle --version'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
