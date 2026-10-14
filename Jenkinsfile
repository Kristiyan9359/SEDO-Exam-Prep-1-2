pipeline {
    agent any

    stages {
        stage('Restore') {
            steps {
                bat 'dotnet restore SoftUniBazar.sln'
            }
        }

        stage('Build') {
            steps {
                bat 'dotnet build SoftUniBazar.sln --no-restore'
            }
        }

        stage('Test') {
            steps {
                bat 'dotnet test SoftUniBazar.sln --no-build --verbosity normal'
            }
        }
    }
}
