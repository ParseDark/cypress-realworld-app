pipeline {
  agent {
    docker {
      args '-p 4000:3000'
      image 'node:12-alpine'
    }

  }
  stages {
    stage('Install') {
      steps {
        sh '''npm config set registry https://registry.npm.taobao.org 

apt-get install chromium-browser

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