pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello Build'
        sleep 10
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Hello Test'
            sleep 10
          }
        }
        stage('Test01') {
          steps {
            echo 'Hello Test01'
            sleep 10
          }
        }
        stage('Test02') {
          steps {
            echo 'Hello Test02'
            sleep 10
          }
        }
        stage('Test03') {
          steps {
            echo 'Hello Test03'
            sleep 10
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Hello Deploy'
        sleep 10
        input(message: 'Deploy to Production', id: 'ProdDeploy', ok: 'OK To Deploy', submitter: 'mdlockwood')
        echo 'Deploying to Production now'
      }
    }
    stage('Final') {
      steps {
        echo 'Hello Final'
        sleep 10
      }
    }
  }
}