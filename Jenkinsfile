pipeline {
    agent any

    stages {
        stage('Install Python') {
            steps {
                sh 'apt-get update || true'
                sh 'apt-get install -y python3 python3-pip || true'
            }
        }

        stage('Check Python') {
            steps {
                sh 'python3 --version'
                sh 'pip3 --version'
            }
        }
    }
}
