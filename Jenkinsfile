pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                echo("Hello Pipeline")
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