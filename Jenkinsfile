pipeline {

  agent {
    node {
     label 'workstation'
   }
  }

  stages {
    stage('one'){
     steps {
       sh 'echo Hello World'
     }
    }
  }
}

  post {
    always {
      sh 'echo Post Cleanup steps'
    }
  }