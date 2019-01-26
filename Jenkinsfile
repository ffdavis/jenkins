def buildNumber = env.BUILD_NUMBER
def workspace = env.WORKSPACE
def buildUrl = env.BUILD_URL

pipeline {
    agent any 
    
    stages {
        
        stage('Stage 1: Hello') {
            steps {
                echo 'Hello world!' 
            }
        }

        stage('Stage 2: Check out Git') {
            steps {
                echo 'Checking out Git'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/samsonawane/SampleProject.git']]])
            }
        }

        stage('Stage3: Status Code Analysis') {
            steps {
                echo 'Static Code Analysis'
                echo "workspace directory is ${workspace}"
                echo "build URL is ${env.BUILD_URL}"
            }
        }
        
        stage('Stage4: Build') {
            steps {
                echo 'Building the Code'
            }
        }

        stage('Stage5: Unit Testing') {
            steps {
                echo 'Unit Testing the Code'
            }
        }

        stage('Stage6: Deliver') {
            steps {
                echo 'Delivering the Code'
            }
        }



    }
}
