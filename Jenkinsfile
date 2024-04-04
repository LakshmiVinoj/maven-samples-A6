pipeline {
  agent any
  tools {
    maven 'maven_var'
    jdk 'java_var'
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/LakshmiVinoj/maven-samples-A6.git', branch specifier: '198644632661c67b6c32f59e9047c11a70685e15')
      }
    }

    stage('run') {
      steps {
        sh 'mvn clean test'
      }
    }
  } 
}
