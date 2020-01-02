  pipeline {
    agent any
      options {
        timestamps()
      }
      stages {
       stage('Checkout') {
          steps {
            checkout scm
        } 
      }
       stage('deploy') {
           steps {
                sh 'echo $HOME'
              }
            }
          }
       }   