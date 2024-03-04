pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS486-1'
                sh 'g++ main1.cpp -o output'
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                sh 'chmod +x output'
                sh './output'
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        failure {
            error 'Pipeline Failed'
        }
    }
}
