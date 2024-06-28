pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                sh "/home/ec2-user/.nvm/versions/node/v20.4.0/bin/npm -v"
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