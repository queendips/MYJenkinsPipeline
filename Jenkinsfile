pipeline {
    agent any

    parameters {
        string(name: 'USERNAME', defaultValue: 'admin', description: 'Enter your username')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests?')
        choice(name: 'ENVIRONMENT', choices: ['dev', 'stage', 'prod'], description: 'Select environment')
    }

    stages {
        stage('Input Summary') {
            steps {
                echo "👤 Username: ${params.USERNAME}"
                echo "🧪 Run Tests: ${params.RUN_TESTS}"
                echo "🌐 Environment: ${params.ENVIRONMENT}"
            }
        }

        stage('Conditional Testing') {
            when {
                expression { return params.RUN_TESTS }
            }
            steps {
                echo '✅ Running tests as requested...'
            }
        }

        stage('Deployment') {
            steps {
                echo "🚀 Deploying to ${params.ENVIRONMENT} environment..."
            }
        }
    }

    
}
