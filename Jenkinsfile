pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'this is to build the app'
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        echo 'this is to test the app'
        sh 'npm test'
      }
    }
    stage('Package') {
      steps {
        echo 'this is to package the app'
        sh 'npm run package'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }
  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'Hello There...This is my first pipeline through code...'
    }
  }
}