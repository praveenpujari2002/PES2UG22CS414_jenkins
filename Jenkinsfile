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
        sh './wrong_executable_name'  // Intentional error
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
