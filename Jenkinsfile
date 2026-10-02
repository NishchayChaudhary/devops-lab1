pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'echo Build completed successfully'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing project...'
                sh 'test -f app.txt'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying project...'
                sh 'mkdir -p deploy'
                sh 'cp app.txt deploy/'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful'
        }
        failure {
            echo 'Deployment failed'
        }
    }
}
