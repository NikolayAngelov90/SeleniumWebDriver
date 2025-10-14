pipeline {
    agent any

    stages {
        stage('Restore Dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Run Project1 Tests') {
            steps {
                bat 'dotnet test Project1 --no-build --verbosity normal'
            }
        }
        stage('Run Project2 Tests') {
            steps {
                bat 'dotnet test Project2 --no-build --verbosity normal'
            }
        }
        stage('Run Project3 Tests') {
            steps {
                bat 'dotnet test Project3 --no-build --verbosity normal'
            }
        }
    }
}