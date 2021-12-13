pipeline {
  agent {
    docker {
      image 'cypress/base'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Install') {
      steps {
        sh '''npm config set registry https://registry.npm.taobao.org 

npm install'''
      }
    }

    stage('Start CI') {
      steps {
        sh 'npm run start:ci'
      }
    }

    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }

  }
}