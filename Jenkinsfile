pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'docker build -t sample-app .'
      }
    }

    stage('Test') {
      steps {
        sh 'npm install'
        sh 'npm test'
      }
    }

    stage('Deploy') {
      steps {
        sh 'skaffold run'
      }
    }
  }
}
