pipeline {
    agent any 
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Restore the project') { 
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build the project') { 
            steps {
                bat 'dotnet build --configuration Release --no-restore'
            }
        }
        stage('Test the project') { 
            steps {
                bat 'dotnet test --no-restore --verbosity normal'   
            }
        }
    }
}
