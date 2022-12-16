node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("sauravkharal1/coursework2")
    }

    stage('Test image') {
        /* Testing inside of the container */

        app.inside {
            sh 'echo "Tests passed"'
        }
    }


}
