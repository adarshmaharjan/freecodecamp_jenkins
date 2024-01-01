pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/adarshmaharjan/freecodecamp_jenkins.git', branch: 'dev')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Frontend Unit Test/ Shell Script') {
          steps {
            sh '''cd curriculum-front && npm i 
'''
          }
        }

      }
    }

  }
}