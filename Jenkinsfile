pipeline {
    agent none

    stages {
        stage('Dotnet') {
            agent {
                image 'mcr.microsoft.com/dotnet/sdk:6.0'
            }
            stages {
                stage('Build') {
                    steps {
                        sh 'dotnet build'
                    }
                }
            }
        }
    }
}