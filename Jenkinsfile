pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:8-alpine'
    }

  }
  stages {
    stage('Build result') {
      steps {
        sh 'docker build -t /example-voting-app-result ./result'
      }
    }
  }
  environment {
    npm_config_cache = 'npm_config_cache'
  }
}