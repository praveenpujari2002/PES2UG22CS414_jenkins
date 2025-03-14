pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG22CS414-1 PES2UG22CS414-1.cpp'  // Compile C++ file
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG22CS414-1'  // Execute compiled file
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
