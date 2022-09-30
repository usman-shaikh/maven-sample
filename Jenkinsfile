pipeline {
  agent any
  tools {
   maven 'maven3'
   jdk 'jdk8' 
  }
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
    stage('Install') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Policy Evaluation') {
      steps {
        echo 'Evaluating'
      }
    }
  }
}
