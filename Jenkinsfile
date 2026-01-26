pipeline {
    agent any

    stages {
        stage('Build') {
                steps {
                    sh '''
                    echo "USER=$(whoami)"
                    echo "PWD=$(pwd)"
                    echo "WORKSPACE=$WORKSPACE"
                    echo "JENKINS_HOME=$JENKINS_HOME"
                    '''
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

