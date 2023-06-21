pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the build the app job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test the app job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package app job'
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
      echo 'Hello this is my first pipeline...'
    }

  }
}