pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make -C main'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
