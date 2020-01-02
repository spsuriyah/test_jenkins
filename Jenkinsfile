  pipeline {
    agent any
      options {
      disableConcurrentBuilds()
      timestamps()
      buildDiscarder(logRotator(numToKeepStr: '10'))
      }
      tools {
        maven 'maven_3.6.3'
      }
      stages {
       stage('clonesources') {
           steps {
                git url: 'https://github.com/spsuriyah/test_jenkins.git'
              }
            }
       stage('build') {
           steps {
                sshagent(credentials : ['ssh_connect']) {
                sh 'mvn --version'
                sh 'mvn clean install'
                sh 'pwd'
                sh 'scp ./target/java-hello-world.war ec2-user@13.127.191.235:/home/ec2-user/'
           }
          }
        }
       }
      }   