pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Application'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/*'
            }
        }
    }
}
