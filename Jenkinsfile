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
            echo "Get Driver Path ${chromeDriverPath}"
          }
        }

        stage('Test Log') {
          steps {
            writeFile(file: 'LogTestFile.txt', text: 'This is an automation file')
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Do you want to deploy?', id: 'ok')
        echo 'Deploy the app in ISS server'
      }
    }

  }
  environment {
    chromeDriverPath = 'C:\\Driver\\Path'
  }
}