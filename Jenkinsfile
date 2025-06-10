pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker {
                    image 'node:lts-alpine'
                }
            } 
            step('test') {
                sh('npm -v')
            }
        }
    }
}