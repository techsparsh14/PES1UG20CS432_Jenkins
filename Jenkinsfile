pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o task5_output task5.cpp'
                build job: 'PES1UG20CS432-1'
            }
        }
        stage('Test') {
            steps {
                sh './task5_output > output.txt'
                sh 'cat output.txt'
            }
        }
        stage('Deploy') {
            steps {
                echos 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
