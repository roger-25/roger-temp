pipeline {
    agent any

    triggers {
        // No need for polling; webhook handles this
    }

    environment {
        BRANCH_NAME = "${env.GIT_BRANCH ?: 'unknown'}"
    }

    stages {
        stage('Deploy if PR Merged') {
            when {
                expression {
                    return env.BRANCH_NAME == 'origin/main' || env.BRANCH_NAME == 'main'
                }
            }
            steps {
                echo "PR merged into ${env.BRANCH_NAME}. Triggering deployment..."
                // Add your real deploy steps here
            }
        }
    }
}
