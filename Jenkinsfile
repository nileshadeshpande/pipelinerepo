pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/nileshadeshpande/pipelinerepo', branch: 'master')
      }
    }
    stage('Unit Testing') {
      parallel {
        stage('Unit Testing') {
          steps {
            sh 'echo \'Unit Tesing\''
          }
        }
        stage('Functional Testing') {
          steps {
            sh 'echo \' Functional Testing run\''
          }
        }
      }
    }
    stage('QA Deployment') {
      steps {
        sh 'echo \' Deployed to QA environment\''
      }
    }
    stage('Production Deployment') {
      steps {
        sh 'echo \'Production Deployment\''
      }
    }
  }
}