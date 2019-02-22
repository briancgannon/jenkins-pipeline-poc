pipeline {
    agent { dockerfile true }
    stages {
        stage('build') {
            steps {
                sh """
                cd python-docker
                docker build -t python-docker-dev .
                docker run --rm -it -p 8080:8080 python-docker-dev
                """
            }
        }
    }
}