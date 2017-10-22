pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh 'mvn clean compile'
      }
    }
    stage('Package') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('Deploy') {
      steps {
        sh 'nohup java -jar target/my-first-app-1.0-SNAPSHOT-fat.jar &'
      }
    }
  }
}