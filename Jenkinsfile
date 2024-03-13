pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'this is the first job'
        sh 'npm install'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'this is the second job'
        sh 'npm test'
      }
    }

    stage('package-the-app') {
      steps {
        echo 'this is the third job'
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