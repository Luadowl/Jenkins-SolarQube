pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Luadowl/Jenkins-SolarQube.git'
            }
        }

        stage('Build and Analyze') {
            steps {
                script {
                    sh 'mvn clean package sonar:sonar -Psonarqube'
                }
            }
        }
    }
}
