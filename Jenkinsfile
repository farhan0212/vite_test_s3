pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker {
                    image 'node:lts-alpine'
                    args '-u root:root -v /var/run/docker.sock:/var/run/docker.sock'
                }
            }
            steps {
                sh('npm run build')
                sh ('ls -l')
            }
        }
    }
}