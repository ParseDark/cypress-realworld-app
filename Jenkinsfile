pipeline {
  agent {
    docker {
      image 'node:8-alpine'
      args '-p 4000:3000'
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