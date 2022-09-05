pipeline {
  agent {
    docker {
      args '-p 3000:3000 -u root'
      image 'node:lts-bullseye-slim'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'export NODE_OPTIONS=--max_old_space_size=1536 && npm install'
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}
