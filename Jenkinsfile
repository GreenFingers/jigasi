pipeline {
  agent {
    docker {
      image 'maven:latest'
      args '-v /root/.m2:/root/.m2'
    }
  }
  triggers {
    pollSCM('')
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
      post {
        always {
          junit 'target/surefire-reports/*.xml'
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Copy package somewhere in some server'      
      }
    }
  }
}
