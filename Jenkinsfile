pipeline {
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