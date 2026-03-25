pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Jenkins has the repository code available here.'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install --upgrade pip'
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest -v'
            }
        }

        stage('Build Message') {
            steps {
                echo 'Build completed successfully.'
            }
        }
    }

    post {
        success {
            echo 'Pipeline finished with SUCCESS.'
        }
        failure {
            echo 'Pipeline finished with FAILURE.'
        }
        always {
            echo 'Pipeline is done.'
        }
    }
}
