pipeline {
    agent { docker 'maven:3-alpine' }
    stages {
        dir('java-web-app') {
            stage('Build') {
                sh 'mvn -B clean verify'
            }
            stage('Run Tests') {
                sh 'mvn test'
            }
        }
    }
}