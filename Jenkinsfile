pipeline {
    agent any

    stages {
        stage('BuildandTest') {
            steps {
                bat "powershell.exe -ExecutionPolicy ByPass -File \"./build.ps1\""
            }
        }
        stage('Publish'){
            steps{
                bat 'dotnet Publish -c Release'
            }
        }
    }
}