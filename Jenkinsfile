pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                sh 'npm install'
            }
        }
    }
    post {
        success {
            echo "Pipeline build"
        }
        cleanup {
            echo "Pipeline clean up"
        }
    }
}