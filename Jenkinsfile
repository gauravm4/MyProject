pipeline {
  agent {
    node {
      label 'MyJenNode1'
    }

  }
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
            echo 'Testing started...'
            sleep 10
            echo 'Testing.... successful'
          }
        }
        stage('Test install') {
          steps {
            echo 'Test install started...'
            sleep 20
            echo 'Testing installation... successful'
          }
        }
        stage('Test upgrade') {
          steps {
            echo 'Test upgrade started...'
            sleep 5
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