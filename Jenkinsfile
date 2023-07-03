pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'sudo docker build -t sample-app .'
      }
    }

    stage('Test') {
      steps {
        sh 'npm install'
      }
    }

    stage('Deploy') {
      steps {
        sh 'skaffold run'
      }
    }
  }
}
