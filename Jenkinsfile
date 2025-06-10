pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                sh('whoami')
            }
        }
        stage('with docker') {
            agent{
                docker {
                    image 'node:20-alpine'
                }
            }
            steps {
                sh '''
                ls -la
                node --version
                npm --version
                npm cache clean --force
                npm install -g npm@latest
                npm --version
                npm ci
                '''
            }
        }
    }
}