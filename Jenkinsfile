pipeline {
  agent any
  stages {
    stage('first') {
      steps {
        parallel(
          "first": {
            sh 'echo Hi'
            
          },
          "first b": {
            mail(subject: 'test', body: 'test', from: 'datta@lemonjolly', to: 'datta@localhost')
            
          }
        )
      }
    }
    stage('second') {
      agent {
          label 'lemony2jenkins'
      }
      steps {
        echo 'hehe'
      }
    }
    stage('third') {
      agent {
          label 'lemony3jenkins'
      }
      steps {
          echo 'JNLP ahoy'
      }
    }
  }
}
