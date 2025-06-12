pipeline {
    agent any

    environment {
        SSH_KEY = credentials('github')
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