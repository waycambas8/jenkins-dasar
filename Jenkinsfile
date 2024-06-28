pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                bat "npm install"
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