pipeline {
    agent any 
    stages {
        stage('Deploy') {
            steps {
                timeout(time:1, unit:"MINUTES") {
                    sh './scripts/holding-by-design.sh'
                }
            }
        }
    }
}