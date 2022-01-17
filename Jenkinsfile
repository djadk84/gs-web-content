pipeline {
  agent any
  tools {
    gradle 'gradle-7.3.3'
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
      }
  }