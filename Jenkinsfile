pipeline {
    agent {
        docker { image 'lockrem/entrypoint-test' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
