pipeline {
    agent {
        docker {
      image 'maven:3.9.9-eclipse-temurin-11'
      args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
      steps {
        echo 'Building JGraphT...'
        sh 'mvn clean compile -B'
      }
        }
        stage('Test') {
      steps {
        echo 'Running tests...'
        sh 'mvn test -B'
      }
        }
        stage('Verify') {
      steps {
        echo 'Running verification...'
        sh 'mvn verify -B'
      }
        }
    }
}
