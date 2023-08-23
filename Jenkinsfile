pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		echo "Build"
                sh 'git fetch'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
		echo "Test"
                sh './jenkins/scripts/test.sh'
            }
        }
	stage('Deploy') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}
