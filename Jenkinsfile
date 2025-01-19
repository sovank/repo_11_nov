pipeline {

    agent any
    environment {
        BRANCH_NAME = 'main' // Setting a custom value
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh "printenv"
            }
        }

        stage('Deploy to Production') {
            when {
                branch 'main'
                }
            
            steps {
                echo "${GIT_BRANCH}"
                echo 'Deploying to production...'
                // Production deployment script goes here
            }
        }
    }

}
