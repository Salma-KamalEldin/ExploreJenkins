pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building ${env.BRANCH_NAME}"
                script {
                env.getEnvironment().each { k, v ->
                    echo "${k}=${v}"
                }
            }
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

