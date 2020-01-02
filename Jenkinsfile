  pipeline {
    node {
     checkout scm
    }
    options {
      timestamps()
    }
    stages {
       stage('deploy') {
           steps {
                sh 'echo $HOME'
              }
            }
          }
       }   