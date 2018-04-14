pipeline {
    agent none
    stages {
        stage('build') {
            agent {
                docker { 
                    image 'maven:3-jdk-8-slim'
                    args '-v /root/.m2:/root/.m2'
                } 
            }
            steps {
                sh 'mvn package'
            }
        }
        
        stage('fuck') {
            agent { 
                docker { 
                    image 'node:6.3' 
                } 
             }
            steps {
                sh 'npm --version'
            }
        }
         stage('run') {
            agent { 
                docker { 
                    image 'openjdk:8-jre' 
                } 
             }
            steps {
                sh 'java -jar target/my-app-1.0-SNAPSHOT.jar'
            }
        }
    }
}
