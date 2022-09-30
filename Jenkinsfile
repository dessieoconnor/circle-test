node {
   
   def app
   
    stage('Checkout code') {
      checkout scm
    }
   
   stage('Build image') {
      app = docker.build("log4j-poc")
      echo 'done build'
   }
   
   stage('Scan') {
      sh '/usr/local/bin/orca-cli -p des-jenkins-docker --api-token "${ORCA_API}" image scan log4j-poc'
   }
    
}
