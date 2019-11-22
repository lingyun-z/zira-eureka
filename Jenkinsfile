pipeline {
  agent any
  environment {
    PROJECT_NAME = "zira-eureka"
  }

  stages {
    stage('build') {
      steps {
        sh "docker build -t ${PROJECT_NAME}:latest ."
      }
    }

    stage('deploy') {
      steps {
        sh "bash deploy.sh ${PROJECT_NAME}"
      }
    }
  }
}
