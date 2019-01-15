pipeline {
  agent any
  stages {
    stage('Build dependencies') {
      steps {
        sh 'npm install'
      }
    }
    stage('Build result') {
      steps {
        sh 'docker build -t dockersamples/result ./result'
      }
    }
  }
}