pipeline {
  agent {
    docker {
      image 'maven:latest'
    }
  }

  stages {
    stage('Build') {
      steps {
        sh 'mvn package'
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
