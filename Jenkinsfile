pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh 'sudo apt update -y'
      }
    }
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            node(label: 'Mynode') {
              dir(path: '/tmp') {
                sh 'echo \'Hello from temp\' >> tmp.txt'
              }

            }

          }
        }
        stage('Build3') {
          steps {
            build(job: 'mvns', propagate: true, quietPeriod: 10, wait: true)
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