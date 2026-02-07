pipeline {
  agent { label 'agent1' }

  environment {
    CI = 'true'
  }

  stages {
    stage('Build') {
      steps {
        sh 'node -v && npm -v'
        sh 'npm ci'
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}
