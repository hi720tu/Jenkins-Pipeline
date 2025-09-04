pipeline {
    agent any

    environment {
        VENV = "venv"
    }

    stages {
        stage('Clone GitHub Repo') {
            steps {
                git branch: 'main', credentialsId: 'github-https', url: 'https://github.com/hi720tu/Jenkins-Pipeline-Python-App.git'
            }
        }

        stage('Set Up Python Virtual Environment') {
            steps {
                sh 'python3 -m venv venv'
                sh './venv/bin/python -m pip install --upgrad.\\venv\\Scripts\\pip install -r requirements.txte pip'
                sh './venv/bin/pip install -r requirements.txt'
            }
        }

        stage('Run Flask App') {
            steps {
                sh './venv/bin/python app.py'
            }
        }
    }
}
