pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git 'https://github.com/AfricanT/java-rest-api-calculator-1.git'
                sh './mvnw clean compile'
                // bat '.\mvnw clean compolie'
            }
        }
        stage('Test') {
            steps {
                sh './mvnm test'
                // bat '.\mvnw test'
            }
        }

        post {
            always {
                junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
    }
}
