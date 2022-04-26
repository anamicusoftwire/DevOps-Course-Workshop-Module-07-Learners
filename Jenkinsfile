pipeline {
    agent none

    environment {
        DOTNET_CLI_HOME = "/tmp/DOTNET_CLI_HOME"
    }

    stages {
        stage('Dotnet') {
            agent {
                docker {
                    image 'mcr.microsoft.com/dotnet/sdk:6.0'
                }
            }
            stages {
                stage('Build Dotnet') {
                    steps {
                        sh 'dotnet build'
                    }
                }
                stage('Test Dotnet') {
                    steps {
                        sh 'dotnet test'
                    }
                }
            }
        }
    }
}