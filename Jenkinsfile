node {
    stage "Prepare environment"
        checkout scm
        def environment  = docker.build 'cloudbees-node'

        environment.inside {
            stage "Checkout and build deps"
                sh "npm install"
        }

    stage "Cleanup"
        deleteDir()
}
