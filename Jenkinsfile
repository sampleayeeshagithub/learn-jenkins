pipeline {
  agent {
    node { label 'workstation' }
  }

  environment {
     SAMPLE_URL = "http://sample.com"
     SSH = credentials("ssh")
  }

  options {
    ansiColor('xterm')
  }

  stages {

    stage('one') {
      steps {
        sh 'echo one'
        sh 'echo ${SAMPLE_URL}'
        sh 'echo $SSH'
      }
    }

    stage('two') {
      steps {
        sh 'echo two'
      }
    }

  }
    post {
       always {
          echo 'Sending Email'
       }
    }
}