pipeline {
    agent any

    environment {
        REPO_URL = 'https://github.com/AdnanLatif/nodejs-ci-cd-pipeline.git'
        SONARQUBE_SERVER = 'SonarQube'
        DOCKER_IMAGE = 'adlatif/nodejs-app'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: env.REPO_URL, branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv(env.SONARQUBE_SERVER) {
                    sh 'npm run sonar'
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    def customImage = docker.build("${DOCKER_IMAGE}:${env.BUILD_ID}")
                    customImage.push()
                }
            }
        }
    }
    
    post {
        always {
            cleanWs()
        }
    }
}
