pipeline {
  agent any
  tools {
      maven 'DHT_MAVEN'
      jdk 'DHT_SENSE'
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/shivalisen/maven-samples.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn test'
        sh 'mvn verify'
        sh 'mvn clean'
      }
    }

  }
}