pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Hello'
      }
    }
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
             echo 'Hello'
           // node(label: 'Mynode') {
              //dir(path: '/tmp') {
                //sh 'echo \'Hello from temp\' >> tmp.txt'
              }

            }

          }
        }
        stage('Build3') {
          steps {
            echo 'Hello'
          }
        }
      }
    }
    stage('Test') {
      steps {
        sleep 1
      }
    }
  }
}
