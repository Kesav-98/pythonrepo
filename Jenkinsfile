pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                echo 'Creating virtual environment and installing dependencies...'
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install --upgrade pip
                    pip install -r requirements.txt
                '''
            }
        }

        stage('Run Python Script') {
            steps {
                echo 'Running main.py...'
                sh '''
                    . venv/bin/activate
                    python main.py
                '''
            }
        }
    }
}
