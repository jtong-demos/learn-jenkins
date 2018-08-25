pipeline {
    agent any
    stages {
        stage("Build"){
            steps{
                sh 'exit 1'
            }
        }
    }
    post {
        failure {
            mail to: "test@example.com",
                 subject: "xxxx ${currentBuild.fullDisplayName}",
                 body: "xxxx ${env.BUILD_URL}"
        }
    }
}