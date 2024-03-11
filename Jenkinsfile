pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'YOUR_PES2UG21CS361-1'
        sh 'gcc -o task5 main/hello.cpp'
        echo 'Build Successful!'
      }
    }
    stage('Test') {
      steps {
        sh './task5'
        echo 'Test Successful!'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Successfully deployed!'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed!'
    }
  }
}
