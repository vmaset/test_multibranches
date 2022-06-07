pipeline {
  agent {
    label 'Linux'
  }
  stages {
    stage ('Test') {
      steps {
        sh 'echo "Test part"'
        sh 'cd /home/jenkins/test_maven'
        sh 'mvn test'
        junit 'reports/**/*.xml'
      }
    stage ('Compile') {
      steps {
        sh 'echo "Compile part"'
        sh 'cd /home/jenkins/test_maven'
        sh 'mvn package'
      }
      stage ('Deploy') {
      steps {
        sh 'echo "Deploy part"'

      }
    }
  }
}
