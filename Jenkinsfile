pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'cd projects/java-gradle && ./gradlew clean build'
            }  
        }
        stage('Test') {
            steps {
                sh 'cd projects/java-gradle && ./gradlew test'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'projects/java-gradle/build/libs/**/*.jar', fingerprint: true
            junit 'projects/java-gradle/build/test-results/**/*.xml'
        }
    }
}