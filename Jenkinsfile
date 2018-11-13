pipeline {
    agent { docker 'maven:3-alpine' }
    stages {
        stage('Build') {
            steps {
                step {
                    checkout scm
                }
                step {
                    dir('java-web-app') {
                        sh 'mvn -B clean verify'
                    }
                }
            }
        }
        stage('Run Tests') {
            steps {
                step {
                    dir('java-web-app') {
                        sh 'mvn test'
                    }
                }
            }
        }
    }
}