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

    stage('HTTP Request') {
      steps {
        httpRequest(url: 'https://eohotv9zrfaegyf.m.pipedream.net', contentType: 'APPLICATION_JSON', httpMode: 'POST', requestBody: '{\\"result\\": \\"${currentBuild.result}\\", \\"message\\": \\"Your custom message here\\"}')
      }
    }

  }
}