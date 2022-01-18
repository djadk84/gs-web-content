pipeline {
  agent any
  tools {
    gradle 'gradle-4.5.1'
    jdk 'java8'
    }
    stages {
      stage('Checkout') {
        steps {
          git branch: 'main', url: 'https://github.com/djadk84/gs-web-content.git'
          }
        }
      stage('Build') {
        steps {
          sh 'gradle clean compileJava'
          }
        }
      stage('Unit-test') {
        steps {
          sh 'gradle test'
          }
        }
      stage('Integration-test') {
        steps {
          sh 'gradle integrationTest'
          }
        }
      }
    post {
      always {
          junit 'build/test-results/**/TEST-*.xml'
        }
      }
  }