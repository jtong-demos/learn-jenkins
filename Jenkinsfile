pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                timeout(time:1, unit:"munites") {
                    retry(5) {
                        sh './scripts/fail-by-design.sh'
                    }
                }
            }
        }
    }
}