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
              git'https://github.com/SitaraMohan/Demo_1.git'
            }
        }

        stage('Build') {
            steps {
                // Build your application
               bat 'echo "Building the application......." '
            }
        }

        stage('Test') {
            steps {
                bat 'echo "Running tests...." '
                }
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your application
                  bat 'echo "Deploying the application...." '
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
