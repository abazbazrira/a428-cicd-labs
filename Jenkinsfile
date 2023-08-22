pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'git fetch'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
