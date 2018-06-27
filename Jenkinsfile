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
      steps {
        sh 'npm run test1'
      }
    }
  }
}