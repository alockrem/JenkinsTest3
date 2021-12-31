pipeline {
    agent {
        docker {
            image 'lockrem/entrypoint-test'
            args '-i --entrypoint='
        }
    }
    stages {
        stage('Generate') {
            steps {
                checkout scm
                stash 'codebase'
            }
        }
        stage('Test') {
            steps {
                unstash 'codebase'
                sh 'node --version'
            }
        }
    }
}
