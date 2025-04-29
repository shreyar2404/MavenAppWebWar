pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK'
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
                sh 'scp target/MavenWebAppWar.war deployuser@192.168.1.100:/opt/tomcat/webapps/'
            }
        }
    }
}
