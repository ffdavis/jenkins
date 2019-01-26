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
        sh 'checkout([$class: \'GitSCM\', branches: [[name: \'*/master\']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: \'https://github.com/samsonawane/SampleProject.git\']]])'
      }
    }
  }
}