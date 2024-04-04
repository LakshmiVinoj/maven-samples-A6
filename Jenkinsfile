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
        sh 'git bisect start'
        sh 'git bisect bad 198644632661c67b6c32f59e9047c11a70685e15'
        sh 'git bisect good 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
        sh 'mvn clean test'
      }
    }
  }
  tools {
    maven 'maven_var'
    jdk 'java_var'
  }
}
