pipeline {
  agent {
    node {
      label 'nodejs'
    }
  }

  stages {
    stage('Run Tests') {
      parallel {
        stage('Backend Tests -2') {
          steps {
            sh 'node ./backend/test.js'
          }
        }
        stage('Frontend Tests -2') {
          steps {
            sh 'node ./frontend/test.js'
          }
        }
      }
    }
  }
}
