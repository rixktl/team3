pipeline {
  agent {
    docker {
      image 'buildkite/puppeteer:latest' 
      args '-p 3000:3000' 
    }
  }
  stages {
    stage('environment') {
      steps {
        sh 'npm install -g npm@latest'
      }
    }
    stage('installation') {
      steps {
        sh 'npm install'
      }
    }
    stage('linting') {
      steps {
        sh 'npm run htmlhint'
        sh 'npm run csslint'
        sh 'npm run eslint'
      }
    }
    stage('testing') {
      steps {
        sh 'npm run test'
      }
    }
    stage('generate docs') {
      steps {
        sh 'npm run generate-docs'
      }
    }
  }
}