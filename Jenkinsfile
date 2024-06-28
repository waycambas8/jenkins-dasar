pipeline {
    agent any
    tools {
        nodejs "node-js"
    }
    stages {
        stage("Npm install") {
            steps {
                sh "npm install"
            }
        }
        stage("Npm Build") {
            steps {
                sh "npm run build"
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