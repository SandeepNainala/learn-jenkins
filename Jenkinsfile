pipeline {

  agent {
    node {
     label 'workstation'
   }
  }

  options {
    ansiColor('Xterm')
  }

  environment {
    SAMPLE_URL = "example.com"
  }

  stages {
    stage('one'){
     steps {
       sh 'echo Hello World'
       sh 'echo Hello Sandeep'
       sh 'echo ${SAMPLE_URL}'
     }
    }
  }

  post {
    always {
      sh 'echo Post Cleanup steps'
    }
  }
}