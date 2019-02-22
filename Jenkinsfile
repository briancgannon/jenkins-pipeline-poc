pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh """
                    echo ${SHELL}
                    pip install --upgrade pip
                    pip install -r requirements.txt 
                """
            }
        }
    }
}