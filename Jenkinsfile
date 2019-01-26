pipeline {
  agent any
  stages {
    stage('Stage 1: Hello') {
      steps {
        echo 'Hello World!'
      }
    }
    stage('Stage 2: Checkout Git') {
      steps {
        echo 'Checking out Git'
        git(url: 'https://github.com/ffdavis/jenkins.git', branch: 'master', changelog: true, poll: true)
      }
    }
  }
}