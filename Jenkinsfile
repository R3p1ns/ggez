pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/R3p1ns/ggez.git'
      }
    }
    stage('Build Docker') {
      steps {
        sh 'docker build -t flask-app .'
      }
    }
    stage('Run Docker') {
      steps {
        sh 'docker run -d -p 5000:5000 flask-app'
      }
    }
  }
}
