pipeline {
  agent {
    node {
      label 'ubuntu-1604-aufs-stable'
    }

  }
  stages {
    stage('Build result') {
      steps {
        sh 'docker build -t dockersamples/result ./result'
      }
    }
  }
}