pipeline {
    agent any

    tools {
        maven 'Maven_3.8.7'
        jdk 'JDK_17'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shreyar2404/MavenAppWebWar.git'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy WAR') {
            steps {
                // Replace with your actual remote details
                sh 'scp target/MavenWebAppWar.war user@your-server:/path/to/tomcat/webapps/'
            }
        }
    }
}
