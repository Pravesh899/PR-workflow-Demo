pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'make build'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'make test'
            }
        }
        stage('Code Analysis') {
            steps {
                sh 'make lint'
            }
        }
    }
    post {
        success {
            script {
                currentBuild.result = "SUCCESS"
            }
        }
        failure {
            script {
                currentBuild.result = "FAILURE"
            }
        }
    }
}
