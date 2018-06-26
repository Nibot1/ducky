pipeline {
  agent any
  stages {
    stage('build web-ext firefox extension') {
      steps {
        sh 'web-ext build /root/ducky/'
      }
    }
  }
}