pipeline {

  agent any

  triggers { pollSCM('H/2 * * * *') }

  options {
    ansiColor('xterm')
  }

  environment {
    SAMPLE_URL = "example.com"
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'MR Jenkins', description: 'who should i say Hello to?')
  }

  stages {
    stage('one'){
     inputs{
       message "DO you Approve?"
       ok "Yes"
     }
     steps {
       sh 'echo Hello World'
       sh 'echo Hello Sandeep'
       sh 'echo ${SAMPLE_URL}'
       sh 'echo PERSON - ${PERSON}'
     }
    }
  }

    stage('Two'){
     when {
       GIT_BRANCH == "origin/test"
     }
     steps {
       sh 'env'
     }
    }

  post {
    always {
      sh 'echo Post Cleanup steps'
    }
  }
}

