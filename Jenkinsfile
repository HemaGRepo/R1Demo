pipeline {
  agent any
  stages {
    stage('Pull from SCM') {
      steps {
        git(url: 'https://github.com/HemaGRepo/R1Demo.git', branch: 'master')
      }
    }
    stage('Move to folder') {
      steps {
        bat 'cd DemoMar\\src'
      }
    }
    stage('Compile') {
      steps {
        bat 'javac DemoMar\\src\\HelloWolrd.java'
      }
    }
    stage('Execute') {
      steps {
        bat 'java DemoMar\\src\\HelloWolrd'
      }
    }
    stage('Result') {
      steps {
        echo 'Completed'
      }
    }
  }
}