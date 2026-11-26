
pipeline {
    agent any

    stages {

        stage('Compile') {
            steps {
                sh 'javac Test.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java Test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
            echo 'This message runs whether pipeline succeeds or fails.'
        }

        success {
            echo 'Build and execution successful!'
        }

        failure {
            echo 'Pipeline failed. Please check Console Output.'
        }

        cleanup {
            echo 'Post execution cleanup completed.'
        }
    }
}
