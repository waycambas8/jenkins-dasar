pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                echo "testing npm"
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