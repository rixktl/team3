pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''npm install -g npm@latest
npm install
'''
      }
    }
    stage('git') {
      steps {
        git(branch: 'jenkins', url: 'https://github.com/rixktl/team3')
      }
    }
  }
}