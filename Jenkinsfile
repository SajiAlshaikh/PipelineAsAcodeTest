pipeline {
  agent any
  stages {
    stage('SCM Checkout') {
      steps {
        build(propagate: true, job: 'AUI-Automation-POC/Get-Latest-Automation-Code-From-Bitbucket')
        archiveArtifacts '**/screenshots/**'
      }
    }

  }
}