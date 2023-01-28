pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "ls"
            }
            post {
                success {
                    echo "success"
                }
                failure {
                    echo "failure"
                }
            }
        }
    }
}
