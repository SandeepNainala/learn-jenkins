pipeline {

  agent any

  options {
    ansiColor('xterm')
  }

  environment {
    SAMPLE_URL = "example.com"
  }

  parameter {
    string(name: 'PERSON', defaultValue: 'MR Jenkins', description: 'who should i say Hello to?')
  }

  stages {
    stage('one'){
     steps {
       sh 'echo Hello World'
       sh 'echo Hello Sandeep'
       sh 'echo ${SAMPLE_URL}'
       sh 'echo PERSON - ${PERSON}'
     }
    }
  }

  post {
    always {
      sh 'echo Post Cleanup steps'
    }
  }
}