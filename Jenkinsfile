pipeline {
  agent any
  stages {
    stage('build web-ext firefox extension') {
      steps {
        sh 'web-ext build'
        sh 'mv web-ext-artifacts/ducky*.zip web-ext-artifacts/ducky.xpi'
        archiveArtifacts(artifacts: 'web-ext-artifacts/ducky.xpi', onlyIfSuccessful: true)
      }
    }
    
  }
}