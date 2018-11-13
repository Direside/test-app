pipeline {
    agent { docker 'maven:3-alpine' }
    stages {
        stage('Build') {
            dir('java-web-app') {
                sh 'mvn -B clean verify'
            }
        }
        stage('Run Tests') {
            dir('java-web-app') {
                sh 'mvn test'
            }
        }
    }
}