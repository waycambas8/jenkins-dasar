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
        stage("Deploy") {
            steps {
                sh "pm2 start dist/main.js -p 3000"
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