pipeline {
  agent any
  stages {
    stage('build web-ext firefox extension') {
      parallel {
        stage('build web-ext firefox extension') {
          steps {
            sh 'web-ext build'
            sh 'mv web-ext-artifacts/ducky*.zip web-ext-artifacts/ducky.xpi'
            archiveArtifacts(artifacts: 'web-ext-artifacts/ducky.xpi', onlyIfSuccessful: true)
          }
        }
        stage('build chrome extension') {
          steps {
            sh 'Xvfb :1 -screen 0 1024x768x24 </dev/null &'
            sh 'export DISPLAY=":1"'
            sh 'google-chrome-stable --pack-extension=./ --pack-extension-key=/root/ducky.pem'
            archiveArtifacts(artifacts: '../ducky.crx', onlyIfSuccessful: true)
          }
        }
      }
    }
  }
}