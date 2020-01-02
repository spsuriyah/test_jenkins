  pipeline {
    agent any
      options {
        timestamps()
      }
      stages {
       stage('clonesources') {
           steps {
                git url: 'https://github.com/spsuriyah/test_jenkins.git'
              }
            }
          }
       }   