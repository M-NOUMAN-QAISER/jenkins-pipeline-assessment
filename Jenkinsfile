pipeline {
    agent any

    stages {
        stage1('Build') {
            steps {
                echo 'Building the code...'
                // Example: sh 'mvn clean install'
            }
        }

        stage2('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
                // Example: sh 'mvn test'
            }
        }

        stage3('Code Analysis') {
            steps {
                echo 'Analyzing code quality...'
                // Example: sh 'sonar-scanner'
            }
        }

        stage4('Security Scan') {
            steps {
                echo 'Performing security scan...'
                // Example: sh 'security-scan-tool'
            }
        }

        stage5('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                // Example: sh 'deploy-script.sh staging'
            }
        }

        stage6('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                // Example: sh 'run-integration-tests.sh staging'
            }
        }

        stage7('Deploy to Production') {
            steps {
                echo 'Deploying to production environment...'
                // Example: sh 'deploy-script.sh production'
            }
        }
    }

    post {
        always {
            mail to: 'developer@example.com',
                 subject: "Pipeline: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                 body: "Status: ${currentBuild.currentResult}. Check the logs for details.",
                 attachLog: true
        }
    }
}
