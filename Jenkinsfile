pipeline {
  stages {
    stage('Checkout') {
      checkout([
        $class: 'GitSCM',
        branches: [[name: '*/main']],
          extensions: [[$class: 'CleanCheckout']],
          userRemoteConfigs: [
            [credentialsId: 'github-user-pass', url: 'https://github.com/usman-shaikh/maven-sample.git']
          ]
      ])  
    }
    stage('Build') {
    }
    stage('Test') {
    }
    stage('Policy Evaluation') {
    }
  }
}
