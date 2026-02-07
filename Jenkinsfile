pipeline {
    agent {
        docker {
          image 'node:10.11.0-alpine'
        }
     }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'node -v'
                sh 'npm -v'
                sh 'npm ci'
            }
        }
        stage('DOING_NOTHING_!') { 
            steps { 
                sh 'echo 1'
                sh 'echo 2'
                sh 'echo 3'
                sh 'echo ...'
            }
        }
        stage('TEST') { 
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}