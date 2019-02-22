pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh """
                    echo ${SHELL}
                    [ -d venv] && rm -rf venv
                    virtualenv venv
                    export PATH=${VIRTUAL_ENV}/bin:${PATH}
                    pip install --upgrade pip
                    pip install -r requirements.txt 
                    make clean                
                """
            }
        }
    }
}