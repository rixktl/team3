pipeline {
  agent any

  tools {nodejs "node"}
  
  stages {
    stage('environment') {
      steps {
        sh 'npm install -g npm@latest'
      }
    }
    stage('build') {
      steps {
        git(branch: 'jenkins', url: 'https://github.com/rixktl/team3')
        sh 'npm install'
      }
    }
  }
}