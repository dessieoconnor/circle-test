pipeline {
  agent {
      docker {
          image 'ubuntu:latest'
          args "-u root"
      }
  }
  stages {
    stage('Docker Build') {
    	agent any
      steps {
      	sh 'docker build -t hello-world:latest .'
      }

    }
    stage('scan') {
          steps {
                 //sh '/usr/local/bin/orca-cli -p des-project --api-token aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== image scan hello-world'
                //sh 'docker run -u 0 --rm -v /var/run/docker.sock:/var/run/docker.sock ghcr.io/orcasecurity/orca-cli:latest -k aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== -p des-jenkins --no-color image scan hello-world'
          }
      }
  }
}
