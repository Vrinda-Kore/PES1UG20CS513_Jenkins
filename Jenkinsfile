pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ -o task5 task5.cpp'
        echo 'Build Stage Successful'
      }
    }
    stage('Test'){
      steps{
        sh 'task5 --test'
        echo 'Test Stage Successful'
      }
    }
    stage('Deploy'){
      steps{
        sh './task5'
        echo 'Deploy Stage Successful'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
