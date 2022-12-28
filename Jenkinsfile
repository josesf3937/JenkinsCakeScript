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
                archiveArtifacts artifacts: 'bin/*/net6.0/*.*', followSymlinks: false, onlyIfSuccessful: true
            }
        }
    }
}