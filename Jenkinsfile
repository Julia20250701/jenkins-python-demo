pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                sh 'which python3 || true'
                sh 'which python || true'
                sh 'which pip3 || true'
                sh 'which pip || true'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python -m pip install --upgrade pip'
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest -v'
            }
        }
    }
}
