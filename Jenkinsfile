pipeline {
    agent { dockerfile true }
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