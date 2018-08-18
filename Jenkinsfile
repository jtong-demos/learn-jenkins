pipeline {
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    sh './scripts/fail-by-design.sh'
                }
            }
        }
    }
}