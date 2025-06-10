pipeline {
    agent any
    stages {
        stage('test') {
          
            steps ('test') {
                sh('whoami')
            }
        }
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