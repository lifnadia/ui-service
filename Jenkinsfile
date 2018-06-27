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
    stage('') {
      steps {
        sh 'npm run test1'
      }
    }
  }
}