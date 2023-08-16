pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }

    stage('error') {
      steps {
        library 'testlib'
        fileExists 'sendFeedback.groovy'
        load 'sendFeedback.groovy'
        sh 'sendFeedback()'
      }
    }

  }
}