pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the C++ program...'
                sh 'g++ main/hello.cpp -o main/hello_exec'
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh './main/hello_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed!'
        }
        success {
            echo 'Pipeline Succeeded!'
        }
    }
}
