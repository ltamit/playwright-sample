pipeline {

  agent any

  tools {
    nodejs "NodeJS16"
  }

  stages {
    stage('Build') {
      steps {
        // One or more steps need to be included within the steps block.
        sh 'git clone git@github.com:ltamit/playwright-sample.git'
        sh 'export LT_USERNAME=${LT_USERNAME}'
        sh 'export LT_ACCESS_KEY=${LT_ACCESS_KEY}'
        sh 'npm install'
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
