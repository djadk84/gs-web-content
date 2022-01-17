pipeline {
  agent any
  tools {
    gradle 'gradle-4.5.1'
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