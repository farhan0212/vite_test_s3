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
                sshagent(credentials: [SSH_CREDENTIALS_ID]) {
                    sh """
                       ssh -o StrictHostKeyChecking=no ${SSH_USERNAME}@${SSH_HOST} '
                        echo "Running commands on remote server"
                        ls -la
                        whoami
                        '
                    """
                }
            }
        }
    }
}