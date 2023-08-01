pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'new_main', credentialsId: '2d710b85-07f5-4d07-a378-5979377da219', url: 'https://github.com/ercuru/vector_role'
                sh 'chmod -R 755 systemctl3.py'
            }
        }
        stage('Molecule') {
            steps {
                sh 'molecule --version'
                sh 'molecule test'
            }
        }
    }
}