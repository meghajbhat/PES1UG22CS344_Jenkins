pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o hello_exec hello.cpp'  // Compiling hello.cpp
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './hello_exec'  // Running the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo Deployment successful!'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Check the logs for errors!'
        }
    }
}
