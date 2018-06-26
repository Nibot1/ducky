pipeline {
  agent any
  stages {
    stage('build web-ext firefox extension') {
      steps {
        sh 'web-ext build -s /root/ducky/'
        sh 'whoami'
      }
    }
  }
}