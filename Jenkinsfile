pipeline {

  agent any

  stages {
    stage('Build') {
      steps {
        // One or more steps need to be included within the steps block.
        sh 'git clone git@github.com:ltamit/playwright-sample.git'
        sh 'npm install'
        sh 'export LT_USERNAME=${LT_USERNAME}'
        sh 'export LT_ACCESS_KEY=${LT_ACCESS_KEY}'
      }

    }

    stage('Test') {
      steps {
        // One or more steps need to be included within the steps block.

        sh 'node playwright-single.js'

      }
    }

  }
}
