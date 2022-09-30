node {
   
   def app
    
   stage('Build image') {
      app = docker.build("log4j-poc")
      echo 'done build'
   }
   
   stage('Scan') {
      sh '/usr/local/bin/orca-cli -p des-project --api-token aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== image scan test-lamp-des-112233'
   }
    
}
