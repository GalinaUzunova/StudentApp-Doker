pipeline {
    agent any

    stages {
        stage('Checkout the repository') {
            steps {
                checkout scm // Pull code from Git
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install' // Install dependencies
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test' // Runs tests
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
        success {
            echo 'Build succeeded'
        }
        failure {
            echo 'Build failed'
        }
    }
}
