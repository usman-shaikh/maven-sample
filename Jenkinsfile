pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout([
          $class: 'GitSCM',
          branches: [[name: '*/main']],
            extensions: [[$class: 'CleanCheckout']],
            userRemoteConfigs: [
              [credentialsId: 'github-user-pass', url: 'https://github.com/usman-shaikh/maven-sample.git']
            ]
        ])
      }
    }
    stage('Build') {
      steps {}
    }
    stage('Test') {
      steps {}
    }
    stage('Policy Evaluation') {
      steps {}
    }
  }
}
