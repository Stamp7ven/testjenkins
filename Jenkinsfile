pipeline {
    agent { label 'centos9-Linux' }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello, Jenkins!' // A simple command to print a message
                sh """
                hostnamectl
                """
            }
        }
    }
}
