pipeline {
    agent {
        docker {
            image 'lockrem/entrypoint-test'
            args '-i --entrypoint='
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
