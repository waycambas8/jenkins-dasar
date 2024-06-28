pipeline {
    agent any
    tools {
        nodejs "node-js" // Ganti dengan nama konfigurasi NodeJS Anda
    }
    stages {
        stage("Hello") {
            steps {
                sh "npm install"
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