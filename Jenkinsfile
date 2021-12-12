pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Install') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Start') { 
            steps {
                sh 'npm run start' 
            }
        }
        stage('Test') { 
            steps {
                sh 'npm run test:headless' 
            }
        }
        stage('Build') { 
            steps {
                sh 'npm run build' 
            }
        }
    }
}