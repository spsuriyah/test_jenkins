  pipeline {
    agent any
      options {
      disableConcurrentBuilds()
      timestamps()
      buildDiscarder(logRotator(numToKeepStr: '10'))
      }
      tools {
        maven 'apache-maven-3.0.1'
      }
      stages {
       stage('clonesources') {
           steps {
                git url: 'https://github.com/spsuriyah/test_jenkins.git'
              }
            }
       stage('build') {
           steps {
                sh 'mvn --version'
           }
          }
        }
       }   