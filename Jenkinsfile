pipeline {
 agent {
 node {
 label 'workstation'
 }
 }
 options {
   ansiColor('xtrem')
   }
   parameters {
      string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
      }

 environment {
   SAMPLE_URL="example.com"
   }

  stages {

    stage('One'){
    input {
      message "Do youn Approve!?"
        ok "Yes"
        }

      steps {
        sh 'echo Hello World'
        sh 'echo Hello Universe'
        sh 'echo ${SAMPLE_URL}'
        sh 'echo PERSON - ${PERSON}'
       }
     }
   stage('Two')
   when {
    GIT_BRANCH == "origin/test"
    }
   steps {
   sh 'env'
    }
   }
 }
