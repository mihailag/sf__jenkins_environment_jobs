pipeline {
    agent any
    parameters {
        choice(
        name: 'SERVER',
        choices: ['all', 'staging', 'production'],
        description: 'Server for reboot'
        )
    }
    stages {
        stage('Build') {
            steps {
                script {
                    if ("${params.SERVER}" == 'all') {
                        sh """
                        ssh staging sudo shutdown -r +1
                        ssh production sudo shutdown -r +1
                        """
                    } else {
                        sh """
                        ssh $SERVER sudo shutdown -r +1
                        """
                    }
                }
            }
        }
    }   
}
