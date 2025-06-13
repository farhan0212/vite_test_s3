pipeline {
  agent {
    label 'docker-nodejs' /
  }
  stages {
    stage('Checkout') {
      steps {
        checkout scm // Harus ini dulu, baru boleh git command lain
      }
    }
    stage('Config Remote') {
      steps {
        sh 'git config remote.origin.url https://github.com/farhan0212/vite_test_s3.git'
      }
    }
  }
}
