pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            bat 'gradle build'
          }
        }

        stage('') {
          steps {
            sh 'gradle build'
          }
        }

      }
    }

    stage('mail Notification') {
      steps {
        mail(to: 'gn_tchoulak@esi.dz', subject: 'build done', body: 'hello world')
      }
    }

  }
}