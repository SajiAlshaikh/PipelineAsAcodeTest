pipeline {
  agent any
  stages {
    stage('SCM Checkout') {
      steps {
        build(propagate: true, job: 'AUI-Automation-POC/Get-Latest-Automation-Code-From-Bitbucket')
        archiveArtifacts '**/screenshots/**'
        slackSend(baseUrl: 'https://hooks.slack.com/services/TAVQ7HRP0/B025YH4ALP3', channel: 'jenkins-pipeline-test', color: 'good', token: 'sHwbs6ZwO4OiDYYnXLvryIqq')
      }
    }

  }
}