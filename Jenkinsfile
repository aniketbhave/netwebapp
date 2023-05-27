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
                bat "msbuild.exe ${workspace}\\WebApplication1.sln /nologo /nr:false  /p:platform=\"x64\" /p:configuration=\"release\" /t:clean;restore;rebuild"
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
