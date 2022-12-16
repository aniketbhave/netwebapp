pipeline {
    agent any
    stages {
        stage('Build') {
            when {
                branch "dev"
            }
            steps {
                echo 'Building..'
                echo 'Hi! from DEV'
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
