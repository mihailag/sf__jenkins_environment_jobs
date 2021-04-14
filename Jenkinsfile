pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh """
                ssh staging uptime
                ssh production uptime
                """
            }
        }
    }   
}