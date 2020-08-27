pipeline {
  agent any
  stages {
    stage('sayHello') {
      steps {
        sh 'echo "Hello World"'
      }
    }

    stage('clear') {
      steps {
        archiveArtifacts(allowEmptyArchive: true, caseSensitive: true, defaultExcludes: true, artifacts: '*.zip')
        timestamps()
      }
    }

  }
  environment {
    Message = 'Hello World'
  }
}