pipeline {
  agent {
      docker {
          image 'ubuntu:latest'
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
              
                sh '''
                  docker run --rm -v /var/run/docker.sock:/var/run/docker.sock ghcr.io/orcasecurity/orca-cli:latest -k aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== -p des-project --no-color image scan hello-world
                '''
          }
      }
  }
}
