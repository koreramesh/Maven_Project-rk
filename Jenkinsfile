pipeline {
    agent any
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
                sh 'cp target/*.war /path/to/tomcat/webapps/'
            }
        }
    }
}
