pipeline {
  agent {
    node {
      label 'slave'
    }

  }
  stages {
    stage('Pre-Build') {
      steps {
        sh 'echo \'Execute Pre-Build Stage........\''
      }
    }

    stage('Build') {
      parallel {
        stage('Build/Linux') {
          steps {
            sh 'echo \'Linux\''
          }
        }

        stage('Build/Widows') {
          steps {
            sh 'echo \'Windows\''
          }
        }

        stage('Build/Mac') {
          steps {
            sh 'echo \'Mac\''
          }
        }

      }
    }

  }
  environment {
    Env = 'QA'
  }
}