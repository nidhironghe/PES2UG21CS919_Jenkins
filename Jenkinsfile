pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        script {
          sh 'g++ -o my_executable a.cpp'
          echo 'Build Stage Successful'
        }
      }
    }
    stage('Test') {
      steps {
        script {
          def output = sh(script: './my_executable', returnStdout: true).trim()
          echo "Output of C++ file: ${output}"
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
