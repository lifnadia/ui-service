pipeline {
  agent {
    node {
      label 'slave'
    }

  }
  stages {
    stage('install') {
      steps {
        sh 'npm install'
      }
    }
    stage('test1') {
      parallel {
        stage('test1') {
          steps {
            sh 'npm run test1'
          }
        }
        stage('test2') {
          steps {
            sh 'npm run test2'
          }
        }
        stage('test3') {
          steps {
            sh 'npm run test3'
          }
        }
      }
    }
    stage('Build Docker') {
      steps {
        sh 'docker build -t lifnadia/ui-service:latest .'
      }
    }
    stage('push to registry') {
      steps {
        sh '''docker push lifnadia/ui-service:latest
'''
      }
    }
  }
}