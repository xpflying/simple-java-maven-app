pipeline {
    agent none
    stages {
        stage('build') {
            agent { docker { image 'maven:3-jdk-8-slim' } }
            steps {
                sh 'mvn package'
                sh 'pwd'
                sh 'ls -l'
            }
        }
        stage('fuck') {
            agent { docker { image 'node:6.3' } }
            steps {
                sh 'npm --version'
            }
        }
    }
}
