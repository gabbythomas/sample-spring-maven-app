pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        label 'compile'
      }
      steps {
        sh 'mvn compile'
      }
    }
    stage("Unit test") {
      agent {
        label 'test'
      }
      steps {
        sh 'mvn test'
      }
    }
  }
  post {
    always {
      // Ideally this is done in parallel or a loop, but this will do for now
      node('compile') {
        cleanWs()
      }
      node('test') {
        cleanWs()
      }
    }
  }
}
