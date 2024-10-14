pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                script {
                    // Clean workspace
                    deleteDir()
                }
            }
        }

        stage('Checkout') {
            steps {
                // Checkout code from the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build your application
                script {
                    // Example build command
                    sh './build.sh'  // Replace with your actual build command
                }
            }
        }

        stage('Test') {
            steps {
                // Run tests
                script {
                    // Example test command
                    sh './test.sh'  // Replace with your actual test command
                }
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your application
                script {
                    // Example deploy command
                    sh './deploy.sh'  // Replace with your actual deploy command
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
