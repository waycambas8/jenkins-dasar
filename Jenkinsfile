pipeline {
    agent any
    tools {
        nodejs "node-js" // Ganti dengan nama konfigurasi NodeJS Anda
    }
    stages {
        stage("Npm install") {
            steps {
                sh "npm install"
            }
        }
    }
    stages {
        stage("Npm Build") {
            steps {
                sh "npm run build"
            }
        }
    }
    stages {
        stage("Npm Start Dev") {
            steps {
                sh "npm run start:dev"
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