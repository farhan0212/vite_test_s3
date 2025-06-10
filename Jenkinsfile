pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker {
                    image 'node:lts-alpine'
                }
            } 
            steps ('test') {
                sh('npm -v')
            }
        }
    }
}