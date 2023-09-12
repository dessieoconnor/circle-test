#!/usr/bin/env groovy
pipeline {
  agent {
      docker: 'Dockerfile.orca' // Use the Dockerfile for Orca
    }
  environment {
    IMAGE_NAME = 'log4j-poc'
    PROJECT_KEY = 'des-jenkins-docker' // Set the desired project for CLI scanning
  }
  stages {
    stage('scan') {
      steps {
        withCredentials([string(credentialsId: 'ORCA_SECURITY_API_TOKEN', variable: 'TOKEN')]) {
          sh '''
            # Run Orca-CLI with the specified project and image
            orca-cli -p ${PROJECT_KEY} image scan ${IMAGE_NAME}
          '''
        }
      }
    }
  }
}
