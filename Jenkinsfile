  pipeline {
    agent any
      options {
        timestamps()
      }
      stages {
       stage('Checkout') {
          checkout scm
        } 
       stage('deploy') {
           steps {
                sh 'echo $HOME'
              }
            }
          }
       }   