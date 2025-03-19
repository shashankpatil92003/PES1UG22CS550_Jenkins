pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output YOUR_SRN-1.cpp' // Replace YOUR_SRN with your actual SRN
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
