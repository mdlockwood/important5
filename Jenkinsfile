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
      steps {
        echo 'Hello Test'
        sleep 10
        sh 'exit 1'
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