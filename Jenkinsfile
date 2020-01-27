pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'gradle build'
      }
    }

    stage('mail Notification') {
      steps {
        mail(to: 'gn_tchoulak@esi.dz', subject: 'build done', body: 'hello world')
      }
    }

  }
}