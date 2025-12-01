pipeline {
    agent any

    stages {
        options { disableConcurrentBuilds(abortPrevious: true) }
        
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

