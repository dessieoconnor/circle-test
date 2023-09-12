node {
   
    stage('Checkout code') {
      checkout scm
    }
   
   stage('Build image') {
      app = docker.build("log4j-poc")
      echo 'done build'
   }
   
   stage('Scan') {
      sh '/usr/local/bin/orca-cli -p des-jenkins-docker --api-token aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxYcFRUb1l2Q1owbW9IZ1lDZTdqN1JGRWlBV3p1ZnhXcw== image scan log4j-poc'
   }
}
