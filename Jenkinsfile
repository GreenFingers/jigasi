pipeline {
  agent {
    docker {
      image 'maven:latest'
      args '-v $HOME/.m2:/root/.m2'
    }
  }

  stages {
    stage('Build') {
      steps {
        echo 'Home is $HOME'
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
