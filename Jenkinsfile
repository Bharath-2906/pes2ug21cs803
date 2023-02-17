pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
          sh 'g++ -o PES2UG21CS803 PES2UG21CS803.cpp'
          build job: 'PES2UG21CS803-1'
      }
    }
    
    stage('Test') {
      steps {
        sh '../PES2UG21CS803'
      }
    }
    
    stage('Deploy') {
      steps {
          echo 'Success'
      }
    }
  }
  
  post {
    failure {
      echo "Ohh no!!..Pipeline failed!!.."
    }
  }
}
