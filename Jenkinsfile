pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'this is to build the app job'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'this is to test the app job'
        sh 'npm test'
      }
    }

    stage('Package') {
      steps {
        echo 'this is to package the app job'
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
      echo 'this pipeline has completed...'
    }

  }
}