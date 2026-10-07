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
            }
        }

        stage('SonarQube Scan') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    bat """
                    sonar-scanner ^
                    -Dsonar.projectKey=jenkins-demo ^
                    -Dsonar.sources=. ^
                    -Dsonar.host.url=http://localhost:9000
                    """
                }
            }
        }
    }
}
