pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS919-1'
          sh 'g++ a.cpp -o output '
        }
    }
    stage('Test') {
      steps {
        sh './output'
        }
      }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
