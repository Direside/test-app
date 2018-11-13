pipeline {
    agent { docker 'maven:3-alpine' }
    stages {
        stage('Build') {
            sh 'mvn -B clean verify'
        }
        stage('Run Tests') {
            sh 'mvn test'
        }
    }
}