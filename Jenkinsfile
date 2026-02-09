pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code from Git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded! Great job.'
        }
        failure {
            echo '❌ Build failed. Please check logs.'
        }
    }
}
