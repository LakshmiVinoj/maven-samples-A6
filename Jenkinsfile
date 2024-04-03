pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/LakshmiVinoj/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn clean test'
      }
    }

  }
  tools {
    maven 'maven_var'
    jdk 'java_var'
  }
}
