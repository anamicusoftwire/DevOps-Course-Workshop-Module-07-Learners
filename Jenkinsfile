pipeline {
    agent none

    // environment {
    //     DOTNET_CLI_HOME = "/tmp/DOTNET_CLI_HOME"
    // }

    stages {
        stage('Dotnet') {
            agent {
                docker {
                    image 'mcr.microsoft.com/dotnet/sdk:6.0'
                }
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