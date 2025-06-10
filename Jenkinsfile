pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker {
                    image 'node:lts-alpine'
                }
            }
            steps {
                sh('npm run build')
                sh ('ls -l')
            }
        }
    }
}