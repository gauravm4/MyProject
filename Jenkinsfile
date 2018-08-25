pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building... successful'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing.... successful'
          }
        }
        stage('Test install') {
          steps {
            echo 'Testing installation... successful'
          }
        }
        stage('Test upgrade') {
          steps {
            echo 'Testing upgrade... successful'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying... successful'
      }
    }
  }
}