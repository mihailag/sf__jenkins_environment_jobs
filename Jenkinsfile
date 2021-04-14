pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh """
                ssh staging sudo docker run --rm -d -p 8080:80 wordpress
                """
            }
        }
    }   
}