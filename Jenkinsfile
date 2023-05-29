@Library ('shared-library')
pipeline {
    agent { label 'windows' }
    stages {
        stage('Build') {
            when {
                branch "dev"
            }
            steps {
                echo 'Building..'
                echo 'Hi! from DEV'
                // cleanWs()
                bat "dotnet restore ${workspace}\\WebApplication1.sln"
                bat "dotnet publish ${workspace}\\WebApplication1.sln -c Release --nologo --no-restore -o ../Publish"
                helloWorld(name: 'aniket', dayOfWeek: 'Sunday')
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
