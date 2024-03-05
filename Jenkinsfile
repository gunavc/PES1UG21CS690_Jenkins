pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG21CS690-1 test.cpp'
                    echo 'Build Stage Successful'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES1UG21CS60-1'
                    echo 'Test Stage Successful'
                }
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
