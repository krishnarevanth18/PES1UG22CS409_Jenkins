pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o gvcd output PES1UG22CS409.cpp'  // Compiling C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Running compiled C++ file
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Step '
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
