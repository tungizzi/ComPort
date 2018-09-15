pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        echo 'Checking code'
      }
    }
    stage('Restore packages') {
      steps {
        echo 'Restoring packages'
        bat 'dotnet restore ComPort.sln'
      }
    }
    stage('Build') {
      steps {
        echo 'Building'
      }
    }
    stage('Test') {
      steps {
        echo 'Test'
      }
    }
    stage('Release') {
      steps {
        echo 'Release'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}