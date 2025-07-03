pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/YOUR_USERNAME/python-jenkins-job.git'
            }
        }

        stage('Setup Python') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate && pip install -r requirements.txt'
            }
        }

        stage('Run Python Script') {
            steps {
                sh '. venv/bin/activate && python main.py'
            }
        }
    }
}
