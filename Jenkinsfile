pipeline {
    agent any

    stages {
        stage('Debug Env') {
            steps {
                echo "Current Branch: ${BRANCH_NAME}"
                echo "Build Number: ${BUILD_NUMBER}"
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
