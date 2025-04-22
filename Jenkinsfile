pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    python3 -m venv venv
                    source venv/bin/activate
                    pip install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    source venv/bin/activate
                    python3 -m pytest
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Despliegue simulado'
            }
        }
    }
}
