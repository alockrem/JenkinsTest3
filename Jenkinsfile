#!groovy

import groovy.json.JsonSlurperClassic

node {
    checkout scm
    /*
     * In order to communicate with the MySQL server, this Pipeline explicitly
     * maps the port (`3306`) to a known port on the host machine.
     */
    docker.image('lockrem/entrypoint-test:latest') { c ->

    }
}
