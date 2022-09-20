pipeline {
    agent { dockerfile true }
    
    stages {
        stage('build') {
  
           app = docker.build("my-image-jenkistest")
            
        }
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
    }

    /*stage('Build image') {

        app = docker.build("test-lamp-des")
        echo 'done build'
    }
    stage('scan') {
        sh '/usr/local/bin/orca-cli -p des-project --api-token aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== image scan test-lamp-des'
    }*/
}
