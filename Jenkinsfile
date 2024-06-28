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
                sh 'node_modules\\.bin\\pm2 start ecosystem.config.js --env dev' 
                sh 'node_modules\\.bin\\pm2 reload all'
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