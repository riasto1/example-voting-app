pipeline {
  agent any
  stages {
    stage('Build result') {
      steps {
        sh 'docker build -t dockersamples/result ./result'
      }
    }
    stage('Build vote') {
      steps {
        sh 'docker build -t dockersamples/vote ./vote'
      }
    }
    stage('Build worker') {
      steps {
        sh 'docker build -t dockersamples/worker ./worker'
      }
    }
    stage('Push result image') {
      steps {
        git(poll: true, url: 'https://github.com/riasto1/example-voting-app', branch: 'master', changelog: true)
      }
    }
  }
  environment {
    npm_config_cache = 'npm_cache'
  }
}