pipeline {
    agent any

    environment {
        name 'admin'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
        stage('Environment Variable') {
            steps {
                echo "name : ${name}"
                echo "Build ID: ${BUILD_ID}"
                sh 'echo "The Jenkins build ID is: $BUILD_ID"'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed.'
        }
    }
}
