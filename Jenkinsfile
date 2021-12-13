pipeline {
  agent {
    docker {
      args '-p 4000:3000'
      image 'cypress/base'
    }

  }
  stages {
    stage('Install') {
      steps {
        sh '''npm config set registry https://registry.npm.taobao.org 

npm install'''
      }
    }

    stage('Start') {
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