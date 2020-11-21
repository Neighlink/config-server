pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '$ ./gradlew build --scan'
      }
    }

    stage('Test') {
      post {
        always {
          junit 'target/surefire-reports/*.xml'
        }

      }
      steps {
        sh 'mvn test'
      }
    }

  }
}