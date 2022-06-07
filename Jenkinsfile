pipeline {
  agent {
    label 'Linux'
  }
  stages {
    stage ('Build') {
      steps {
        sh 'echo "Build part"'
        sh 'make'
      }
    stage ('Test') {
      steps {
        sh 'echo "Test part"'
        sh 'make check'
        junit 'reports/**/*.xml'
      }
    stage ('Deploy') {
      steps {
        sh 'echo "Deploy part"'
        sh 'make publish'
      }
    }
  }
}
