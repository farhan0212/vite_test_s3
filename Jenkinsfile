pipeline {
    agent any

    environment {
        SSH_CREDENTIALS_ID = '26dc69fa-f0a0-4c62-8f3d-2d76a25701b4'
        SSH_HOST = '159.223.95.88'
        SSH_USERNAME = 'github'
    }
    stages {
        stage('Remote ssh') {
            steps {
                sshCommand remote:  [
                    name: 'remote-server',
                    host: env.SSH_HOST,
                    port: 22,
                    credentialsId: env.SSH_CREDENTIALS_ID,
                    username: env.SSH_USERNAME
                ], command: 'ls -la'
            }
        }
    }
}