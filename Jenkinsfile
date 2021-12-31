pipeline {
    agent {
        docker {
            image 'lockrem/entrypoint-test'
            args '-i --entrypoint='
        }
    }
    stages {
        stage('Generate') {
            checkout scm
            stash 'codebase'
        }
        stage('Test') {
            steps {
                unstash 'codebase'
                sh 'node --version'
            }
        }
    }
}
