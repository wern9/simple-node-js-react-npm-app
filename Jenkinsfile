pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:lts-bullseye-slim'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

  }
}