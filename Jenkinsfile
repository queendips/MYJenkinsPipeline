pipeline {
    agent any

    environment {
        NAME = 'admin'        // Define a meaningful environment variable
        LOCATION = 'India'    // Another example
    }

    stages {
        stage('Build') {
            steps {
                echo '🔧 Building...'
            }
        }

        stage('Test') {
            steps {
                echo '✅ Testing...'
            }
        }

        stage('Deploy') {
            steps {
                echo '🚀 Deploying...'
            }
        }

        stage('Environment Variable') {
            steps {
                echo "👤 Name: ${env.NAME}"
                echo "🌍 Location: ${env.LOCATION}"
                echo "🆔 Build ID: ${env.BUILD_ID}"
                sh '''
                    echo "=== Shell Output ==="
                    echo "Name from shell: $NAME"
                    echo "Location from shell: $LOCATION"
                    echo "Jenkins Build ID: $BUILD_ID"
                '''
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
