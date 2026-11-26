
pipeline {
    agent any

    stages {

        stage('Compile') {
            steps {
                sh 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java HelloWorld'
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
