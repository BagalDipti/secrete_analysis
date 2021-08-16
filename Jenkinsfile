pipeline {
  
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git 'http://gsgit.gslab.com/dipti_bagal/secrets_analysis.git'
      }
    }

stage('Check-Git_Secrets'){
  steps {
      sh 'docker run gesellix/trufflehog --json http://gsgit.gslab.com/dipti_bagal/DevSecOps_bk.git > trufflehog'
      sh 'cat trufflehog'
      }
  }
