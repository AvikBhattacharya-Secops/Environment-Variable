pipeline {
    agent any

    environment {
        // Define environment variable (can also come from Jenkins credentials)
        BRANCH_NAME = 'main'
        GITHUB_REPO = 'https://github.com/<your-username>/<your-repo>.git'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: "${BRANCH_NAME}", url: "${GITHUB_REPO}"
            }
        }

        stage('Build') {
            steps {
                echo "Building the code from ${GITHUB_REPO} on branch ${BRANCH_NAME}"
                // Add your build steps here
            }
        }
    }
}
