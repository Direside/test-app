pipeline {
    agent {
        docker { image 'maven:3.6.0-jdk-8-alpine' }
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                dir('java-web-app') {
                    sh 'mvn -B clean verify'
                }
            }
        }
        stage('Run Tests') {
            steps {
                dir('java-web-app') {
                    sh 'mvn test'
                }
            }
        }
    }
}
