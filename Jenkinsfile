pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'From Build Stage'
      }
    }

    stage('Test') {
      parallel {
        stage('Test 1') {
          steps {
            echo 'From Test Stage 1'
          }
        }

        stage('Test 2') {
          steps {
            echo 'From Test Stage 2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'From Deploy Stage'
      }
    }

  }
}