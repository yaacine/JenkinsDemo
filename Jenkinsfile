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
        mail(to: 'gn_tchoulak@esi.dz', subject: 'build done', body: 'hello world', from: 'test@esi.dz')
      }
    }

    stage('sonarQube') {
      steps {
        withSonarQubeEnv('sonar') {
          bat 'gradle sonarqube'
          waitForQualityGate(credentialsId: 'sonar', abortPipeline: true)
        }

      }
    }

  }
}