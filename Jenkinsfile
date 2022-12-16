pipeline {
    agent any

    stages {
        stage('Build') {
            when {
                branch "dev"
            }
            steps {
                echo 'Building..'
                enco 'Hi! from DEV'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
