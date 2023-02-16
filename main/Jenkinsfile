pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
        echo 'Build Stage successful'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
        echo 'Test Stage Successful'
        post {
          always {
            junit 'target/surefire-reports/*.xml'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn deploy'
        scho 'Deployment success!'
      }
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
