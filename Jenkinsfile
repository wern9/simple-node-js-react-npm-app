pipeline {
  agent {
    docker {
      args '-p 3000:3000 -p 5000:5000 -u root'
      image 'node:lts-bullseye-slim'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install -g increase-memory-limit && npm install'
      }
    }

  }
}