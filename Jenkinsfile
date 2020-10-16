def CREDENTIALS_ID = 'jenkins.ssh'
def ZMHXCLIENT_REPO = 'git@git.shiyou.kingsoft.com:zmhx/zmhx-client.git'
pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        script {
          checkout([$class: 'GitSCM', branches: [[name: 'master']], userRemoteConfigs: [[credentialsId: CREDENTIALS_ID, url: ZMHXCLIENT_REPO]]])
        }
      }       
    }  
    stage('sayHello') {
      steps {
        sh 'echo "Hello World #4"'
      }
    }
  }
}
