pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        node {
          label 'master'
        }

      }
      steps {
        sh 'sh mvn clean package'
      }
    }

    stage('git') {
      steps {
        git(poll: true, url: 'https://github.com/greenlinkway/jenkinsfile.git', branch: 'main')
      }
    }

  }
}