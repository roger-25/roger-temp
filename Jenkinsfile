pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building code on branch: ${env.BRANCH_NAME}"
            }
        }
        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }
    }
    post {
        success {
            echo "Pipeline Success"
        }
        failure {
            echo "Pipeline Failed"
        }
    }
}
