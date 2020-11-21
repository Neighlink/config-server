pipeline {
  agent {
    dockerfile {
      filename 'jenkinsfile'
    }

  }
  stages {
    stage('Build') {
      steps {
        withGradle()
      }
    }

  }
}