pipeline {

  agent any
  stages {
    stage ('Install node modules') {
      steps {
        sh "npm install"
      }
    }
    stage('Running tests'){
      steps {
        sh "npm test"
      }
    }
    stage('Building app'){
      steps {
        sh "npm run build"
      }
    }
    stage('Deploying app') {
      steps {
        sh 'pm2 serve build 4005 --watch'
      }
    }
  }
}