node {
    def app

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("hello-world")
        echo 'done build'
    }
    stage('scan') {
        sh '/usr/local/bin/orca-cli -p des-project --api-token aHR0cHM6Ly9hcHAuYXUub3JjYXNlY3VyaXR5LmlvfHxpWDhiS0NaWkhRRk90VGJPcERMZ2tCYkRCNUZFT2NjSw== image scan hello-world'
    }
}
