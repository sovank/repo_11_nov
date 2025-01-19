pipeline {

    agent any

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
                "${env.BRANCH_NAME}" 'main'
            }
            
            steps {
                echo 'Deploying to production...'
                // Production deployment script goes here
            }
        }
    }

}
