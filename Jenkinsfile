pipeline {
    agent any

    environment {
        SSH_KEY = credentials('26dc69fa-f0a0-4c62-8f3d-2d76a25701b4')
        SSH_HOST = '159.223.95.88'
    }
    stages {
        stage('Remote ssh') {
            steps {
                sshCommand remote:  [
                    host: env.SSH_HOST,
                    port: 22,
                    credentialsId: env.SSH_KEY,
                    username: 'github'
                ], command: 'ls -la'
            }
        }
    }
}