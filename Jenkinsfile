pipeline {
  agent any
  tools {
    nodejs 'NodeJS 4.8.6'
  }
  stages {
    stage('build') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('Package') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
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
