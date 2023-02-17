pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c main/PES2UG21CS803.cpp'
                sh 'g++ -o PES2UG21CS803 main/PES2UG21CS803.cpp'
                echo 'build stage successfull'
            }
        }
        stage('Test'){
            steps{
                sh './PES2UG21CS803'
                echo 'test stage successful'
            }
        }
        stage('Deploy'){
            steps{
          
                echo 'Deployment Successful'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
