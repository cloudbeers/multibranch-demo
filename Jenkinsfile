
node('master') {
    try {
        stage('build') {
            // Checkout the app at the given commit sha from the webhook
            error("Build failed because of this and that..")
            // Install dependencies, create a new .env file and generate a new key, just for testing

            // Run any static asset building, if needed
            // sh "npm install && gulp --production"
        }

        stage('test') {
            // Run any testing suites
            sh "./vendor/bin/phpunit"
        }

        stage('deploy') {
            // If we had ansible installed on the server, setup to run an ansible playbook
            // sh "ansible-playbook -i ./ansible/hosts ./ansible/deploy.yml"
            sh "echo 'WE ARE DEPLOYING'"
        }
    } catch(error) {
        throw error
    } finally {
        // Any cleanup operations needed, whether we hit an error or not
    }

}