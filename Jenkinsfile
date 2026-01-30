pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo apt install npm'
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