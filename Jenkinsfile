pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 31001:3000'
        }
    }
    environment {
       CI = 'true'
   }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
          steps {
              sh './jenkins/scripts/test.sh'
          }
      }
    }
}
