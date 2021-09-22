pipeline {
  agent any
  stages {
    stage('one') {
      steps {
        echo 'this is the first job'
        sh 'uptime'
        sleep 4
      }
    }

    stage('two') {
      steps {
        echo 'this is the second job'
        sh 'uptime'
        sleep 9
      }
    }

    stage('three') {
      steps {
        echo 'this is the third job'
        sh 'uptime'
        sleep 7
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}