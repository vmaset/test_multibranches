pipeline {
  agent {
    label 'Linux'
  }
  stages {
    stage ('Build') {
      steps {
        sh 'echo "Build part"'
        sh 'cd /home/jenkins/test_maven'
        sh 'mvn validate'
        sh 'mvn compile'
        sh 'mvn package'
      }
    stage ('Test') {
      steps {
        sh 'echo "Test part"'
        sh 'cd /home/jenkins/test_maven'
        sh 'mvn test'
        junit 'reports/**/*.xml'
      }
    stage ('Deploy') {
      steps {
        sh 'echo "Deploy part"'

      }
    }
  }
}
