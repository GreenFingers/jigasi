pipeline {
  agent {
    docker {
      image 'webratio/ant'
    }
  }

  stages {
    stage('Build') {
      steps {
        sh 'ant make'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
        echo 'Testing 1'
        echo 'Testing 2'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying..'
      }
    }
  }
}
