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
        sh 'npm install'
      }
    }
  }
}