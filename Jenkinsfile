pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''date
pwd
ls
mvn --version'''
        tool 'maven'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'hello'
            sleep 5
          }
        }

        stage('test-env') {
          steps {
            echo 'test-env'
          }
        }

      }
    }

    stage('prod') {
      steps {
        echo 'prod'
      }
    }

  }
}