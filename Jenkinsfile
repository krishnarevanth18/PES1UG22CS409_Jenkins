pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ vdvgwd PES1UG22CS409.cpp -o PES1UG22CS409'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS409'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
