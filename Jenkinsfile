pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "This is Build stage."
                build 'PES1UG21CS223-1'
                sh 'g++ ./bye.cpp -o output'
                echo "Build Stage Successful"
            }
        }
        stage('Test') {
            steps {
                echo "This is Test stage." 
                sh 
                echo "Test Stage Successful"
            }
        }
        stage('Deploy') { 
            steps {
                echo "This is Deploy stage."
                echo "Deployment Success"
            }
        }
    }
    post{
        failure{
            error 'Pipeline Failed'
        }
    }
}
