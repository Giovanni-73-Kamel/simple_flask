pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.withRegistry('https://index.docker.io/v1/', 'dockerhub') {
                        def customImage = docker.build("giovanni37/flask-app:v1")
                        customImage.push()
                    }
                }
            }
        }
    }
}
