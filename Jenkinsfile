pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh 'sudo apt update -y'
      }
    }
    stage('Build') {
      steps {
        node(label: 'Mynode') {
          dir(path: '/tmp') {
            sh 'echo \'Hello from temp\' >> tmp.txt'
          }

        }

      }
    }
  }
}