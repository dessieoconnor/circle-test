node {
   
   def app
   agent { dockerfile true }
   
   stage('checkout scm') {
      steps { 
         script{
            checkout scm
         }
       }
   }
   
   stage('Build image') {
      app = docker.build("log4j-poc")
      echo 'done build'
   }
   
   stage('Scan') {
      sh '/usr/local/bin/orca-cli -p des-jenkins-docker --api-token aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== image scan log4j-poc'
   }
    
}
