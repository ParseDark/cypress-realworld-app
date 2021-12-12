pipeline {
  agent any
  stages {
    stage('npm install') {
      steps {
        sh 'npm install'
      }
    }

    stage('npm start') {
      steps {
        sh 'npm run start'
      }
    }

    stage('npm run test') {
      steps {
        sh ' npm run test:headless'
      }
    }

    stage('npm run build') {
      steps {
        sh 'npm run build'
      }
    }

  }
}