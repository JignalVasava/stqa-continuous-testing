pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/JignalVasava/stqa-continuous-testing'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'pytest'
            }
        }
    }
}