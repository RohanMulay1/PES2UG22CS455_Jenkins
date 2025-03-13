pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'g++ -o output main.cpp' // Compiles a C++ file (modify filename if needed)
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './output' // Execute compiled file (change according to your test)
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo "Deployment successful!"'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline completed successfully'
        }
    }
}
