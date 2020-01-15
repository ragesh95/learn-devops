pipeline {
    agent any
    stages {
      stage('One') {
        steps {
          echo "Hi, this is test"
        }
      }
      stage('Two') {
        steps {
          input('Do you want to continue?')
        }
      }
      stage('Three') {
        when {
          not {
            branch "master"
          }
        }
        steps {
          echo "No branch"
        }
      }
      stage('Four') {
        parallel {
          stage('Unit Test') {
            steps {
              echo "Running Unit Test"
            }
          }
        }
      }
    }
}
