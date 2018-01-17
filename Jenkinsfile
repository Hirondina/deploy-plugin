pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git 'https://github.com/Hirondina/deploy-plugin.git'
      }
    }
    stage('Test') {
      steps {
        junit 'TEST-InjectedTest.xlm'
      }
    }
    stage('Deploy') {
      steps {
        awaitDeployment(threshold: 1, env: 'hirocorreia1994@gmail.com')
      }
    }
  }
}