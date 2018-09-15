pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        echo 'Checking code....'
        echo "Job '${JOB_NAME}' (${BUILD_NUMBER}) is waiting for input"
      }
    }
    stage('Restore packages') {
      steps {
        echo 'Restoring packages....'
        bat 'dotnet restore ComPort.sln'
      }
    }
    stage('Build') {
      steps {
        echo 'Building....'
        bat "dotnet clean ComPort.sln"
        bat "dotnet build ComPort.sln -c Debug /property:Version=1.0.${BUILD_NUMBER}"
      }
    }
    stage('Test') {
      steps {
        echo 'No Testing....'
				//bat 'dotnet test ./ComPort.Test/'
      }
    }
    stage('Release') {
      steps {
        echo 'No Release'
        //bat "dotnet build ComPort.sln -c Release /property:Version=2.1.${BUILD_NUMBER}"
      }
    }
    stage('Deploy') {
      steps {
        echo 'No Deploy'
        //bat "copy .\\ComPort\\bin\\Release\\*.nupkg C:\\Host\\packages\\ /Y"
      }
    }
  }
}
