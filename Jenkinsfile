pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        https://github.com/koreramesh/Maven_Project-rk.git
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('Deploy') {
      steps {
        deploy adapters: [tomcat8(credentialsId: 'your-tomcat-cred-id', url: 'http://localhost:8080')], war: '**/target/*.war'
      }
    }
  }
}
