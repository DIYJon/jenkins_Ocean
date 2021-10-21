pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'python --version'
          }
        }

        stage('Test 1') {
          steps {
            echo 'Test'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy'
        sh 'echo "Second step"'
        sleep 1
      }
    }

  }
   post{
    cleanup{
      
    }
    success{

    }
  }
}
