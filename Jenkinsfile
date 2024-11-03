node {
  enviorment {
    DOCKER_IMAGE = 'with-sonar-analysis'
  }
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
  stage('Build Docker Image') {
    steps {
        // Build the Docker image from the checked-out code
        script {
            sh "docker build -t ${DOCKER_IMAGE}:latest ."
        }
    }
  }
}