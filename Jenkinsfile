pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                sh "git branch"
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