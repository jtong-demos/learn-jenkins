pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'echo "Failed"; exit 1'
            }
        }
    }

    post {
        always {
            echo 'This is will always run'
        }
        success {
            echo 'This will run only if success'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of Pipeline has changed'
            echo 'for example, if the Pipeline was prrviously but is now successful'
        }
    }
}