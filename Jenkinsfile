pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building...'
          }
        }

        stage('error') {
          steps {
            library 'testlib'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }

    stage('error') {
      steps {
        script {
          post {
            always {
              script {
                sendFeedback()
              }
            }
          }
        }

      }
    }

  }
}