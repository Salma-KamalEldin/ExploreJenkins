pipeline {
    agent any

    options { disableConcurrentBuilds(abortPrevious: true) }

    stages {
        
        stage('Build') {
            steps {
                echo "Building ${env.BRANCH_NAME}"
            }
        }

        stage('Test') {
            steps {
                echo "Running tests on ${env.BRANCH_NAME}"
            }
        }
        stage('Long Task') {
            steps {
                echo "Starting long job…"
                sleep time: 5, unit: 'MINUTES'
                echo "Long job finished."
            }
        }
    }

    post {
        success {
            echo "Build succeeded on ${env.BRANCH_NAME}"
        }
        failure {
            echo "Build failed on ${env.BRANCH_NAME}"
        }
    }
}

