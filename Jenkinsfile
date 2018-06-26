pipeline {
  agent any
  stages {
    stage('build web-ext firefox extension') {
      steps {
        sh 'whoami'
        sh 'web-ext build'
      }
    }
  }
}