pipeline {
    agent {
        docker { image 'lockrem/entrypoint-test:latest' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
