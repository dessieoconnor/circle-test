#!/usr/bin/env groovy

pipeline {
  agent {
    dockerfile {
      filename: 'Dockerfile.orca' // Use the Dockerfile for Orca
    }
  }
  environment {
    IMAGE_NAME = '<image name>'
    PROJECT_KEY = 'des-jenkins-docker' // Set the desired project for CLI scanning
  }
  stages {
    stage('scan') {
      steps {
        withCredentials([string(credentialsId: 'aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxGUHpIMVhpN3dqRUx0eXM2d2IzY2RyMkdvZUpDRWdzbQ==', variable: 'TOKEN')]) {
          sh '''
            # Run Orca-CLI with the specified project and image
            orca-cli -p ${PROJECT_KEY} image scan ${IMAGE_NAME}
          '''
        }
      }
    }
  }
}
