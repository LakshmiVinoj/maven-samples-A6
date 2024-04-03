pipeline {
  agent any
  tools {
    maven 'maven_var'
    jdk 'java_var'
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/LakshmiVinoj/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify clean test'
      }
    }
  } 
}
