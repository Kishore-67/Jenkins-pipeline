pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the Docker image...'
                sh 'docker build -t simple-app .'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests (pretend tests)...'
                sh 'echo "Tests passed!"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the Docker container...'
                sh 'docker run -d -p 8080:80 simple-app'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution complete.'
        }
    }
}
