pipeline {
    agent {
        docker {
            image 'lockrem/entrypoint-test'
            args '-it'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
