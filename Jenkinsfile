node {
  
  environment {
    DOCKER_IMAGE = 'with-sonar-analysis'
  }

  stage('SCM') {
    checkout scm
  }

  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner'
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }

  stage('Build Docker Image') {
    script {
      sh "docker build -t ${env.DOCKER_IMAGE}:latest ."
    }
  }
}
