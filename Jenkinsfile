pipeline {
    agent any

  stages {
        stage('Build') {
            steps {
                echo "Running build for branch: ${env.BRANCH_NAME}"
            }
        }
        stage('Deploy Only If PR is Merged to Main') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying after PR merged into main!"
                // Add your deployment steps here
            }
        }
    }
}
