pipeline {
  agent {
    docker {
      image 'chmod +x gradlew'
      args './gradlew build'
    }

  }
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