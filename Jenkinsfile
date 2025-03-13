pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS575-1'
                sh 'g++ add2.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
