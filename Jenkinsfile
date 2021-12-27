#!groovy

import groovy.json.JsonSlurperClassic

node {

    def toolbelt = tool 'toolbelt'

    // -------------------------------------------------------------------------
    // Check out code from source control.
    // -------------------------------------------------------------------------

    stage('checkout source') {
        checkout scm
    }

    // -------------------------------------------------------------------------
    // Deploy to DevHub
    // -------------------------------------------------------------------------
    
    stage('Deply to DevHub') {
        rc = command "${toolbelt}/sfdx force:source:deploy -p force-app -u DevHub"
        if (rc != 0) {
            error 'Deployment to DevHub failed.'
        }
    }
}

def command(script) {
    if (isUnix()) {
        return sh(returnStatus: true, script: script);
    } else {
        return bat(returnStatus: true, script: script);
    }
}
