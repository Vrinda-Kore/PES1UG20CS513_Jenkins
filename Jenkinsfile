pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Stage successful'
      }
    }
    stage('Test') {
      steps {
        echo 'Test Stage Successful'
//         post {
//           always {
//             junit 'target/surefire-reports/*.xml'
//           }
//         }
      }
    }
    stage('Deploy') {
      steps {
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
