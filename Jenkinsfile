pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'Building the application\''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo \'Testing the application\''
          }
        }

        stage('test1') {
          steps {
            sh 'echo \'Running test 1\''
          }
        }

        stage('test2') {
          steps {
            sh 'echo \'running test 2\''
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'are you sure ', ok: 'yes i\'m sure')
        sh 'echo \'deploy the application\''
      }
    }

  }
}