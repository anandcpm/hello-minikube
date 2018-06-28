pipeline {
   agent {
    kubernetes {
      label 'kubernetes'
      containerTemplate {
        name 'maven'
        image 'maven:3.3.9-jdk-8-alpine'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  stages {
    stage('Hello MiniKube!') {
      steps {
        echo 'Hello Mini K8s'
      }
    }
    stage('Maven in k8s') {
      steps {
        container('maven') {
          sh 'mvn -version'
        }
      }
    } 
  }
}
