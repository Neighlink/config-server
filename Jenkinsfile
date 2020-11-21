pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        withGradle()
        git(url: 'https://github.com/Neighlink/config-server.git', branch: 'develop/azure')
      }
    }

  }
}