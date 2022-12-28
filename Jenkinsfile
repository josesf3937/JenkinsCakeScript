pipeline {
    agent any
    environment{
        FilePath='**/bin/Release/net6.0/*.*'
    }

    stages {
        stage('BuildandTest') {
            steps {
                bat "powershell.exe -ExecutionPolicy ByPass -File \"./build.ps1\""
            }
        }
        stage('Publish'){
            steps{
                archiveArtifacts artifacts: ${FilePath} , followSymlinks: false, onlyIfSuccessful: true
            }
        }
    }
}