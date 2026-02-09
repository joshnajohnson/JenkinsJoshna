pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/joshnajohnson/JenkinsJoshna.git', branch: 'master'
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling source code...'
                bat 'javac Hello.java'
            }
        }

        stage('Archive Artifacts') {
            steps {
                echo 'Archiving build artifacts...'
                archiveArtifacts artifacts: '**/*.class', fingerprint: true
            }
        }
    }

    post {
        success {
            echo '✅ CI pipeline completed successfully!'
        }
        failure {
            echo '❌ CI pipeline failed. Please check logs.'
        }
    }
}
