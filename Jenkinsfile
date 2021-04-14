pipeline {
    agent any
    triggers {
      cron '*/5 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                sh """
                ping -c 1 staging
                ping -c 1 production
                """
            }
        }
    }   
}