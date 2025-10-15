pipeline {
    agent any
    environment {
        TOMCAT_PATH = '/opt/tomcat/webapps/' // replace with your Tomcat path
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/koreramesh/Maven_Project-rk.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp target/*.war $TOMCAT_PATH'
            }
        }
    }
}
