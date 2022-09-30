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
    stage('Build') {
      steps {
        sh 'mvn clean install -DskipTests'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Policy Evaluation') {
      steps {
        echo 'Evaluating'
      }
    }
  }
}
