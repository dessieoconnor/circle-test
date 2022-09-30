node {
   
   def app
    
   stage('Build image') {
      app = docker.build("log4j-poc",  "--pull /var/lib/jenkins/workspace/Dessie Shift Left/")
      echo 'done build'
   }
   
   stage('Scan') {
      sh '/usr/local/bin/orca-cli -p des-jenkins-docker --api-token aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== image scan log4j-poc'
   }
    
}
