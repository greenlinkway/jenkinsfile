pipeline {
  agent {
    node {
      label 'qubes_slave'
    }

  }
  stages {
    stage('stage1') {
      agent {
        node {
          label 'qubes_slave'
        }

      }
      steps {
        sh 'echo \'Hello World\''
      }
    }

    stage('stage2') {
      agent {
        node {
          label 'qubes_slave'
        }

      }
      environment {
        FUCK = '888'
      }
      steps {
        sh 'echo "Hello $FUCK"'
      }
    }

    stage('stage3') {
      steps {
        sh 'echo \'Hello World2\''
        sleep 5
        echo 'Hello step3'
      }
    }

  }
}