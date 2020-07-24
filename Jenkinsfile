pipeline {
  agent any
  stages {
    stage('Build') {
      environment {
        chromeDriverPath = 'c:\\driver\\path'
      }
      parallel {
        stage('Build') {
          steps {
            echo 'Building java application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the application'
            echo '"Get Driver Path ${chromeDriverPath}"'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy the app in ISS server'
      }
    }

  }
  environment {
    chromeDriverPath = 'C:\\Driver\\Path'
  }
}