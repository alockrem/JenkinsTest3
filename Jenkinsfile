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
                sf 'sfdx force:org:list'
                sh 'node --version'
            }
        }
    }
    post {
        mail to: lockrem@gmail.com, subject: 'Pipeline failed...'
    }
}
