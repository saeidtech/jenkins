pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(branch: 'master', url: 'git@github.com:saeidtech/jenkins.git')
      }
    }
    stage('Build') {
      steps {
        sh 'sh "mvn clean compile"'
      }
    }
    stage('Test') {
      steps {
        sh 'sh "mvn test"'
      }
    }
  }
}