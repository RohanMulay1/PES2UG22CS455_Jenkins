pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS455-1 main.cpp' // Compile the .cpp file
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS455-1' // Run the compiled program
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

