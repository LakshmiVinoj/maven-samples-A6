pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/LakshmiVinoj/maven-samples-A6.git', branch: '198644632661c67b6c32f59e9047c11a70685e15')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify clean test'
      }
    }

    stage('checkout2') {
      steps {
        git(url: 'https://github.com/LakshmiVinoj/maven-samples-A6.git', branch:[[name: '98ac319c0cff47b4d39a1a7b61b4e195cfa231e5']])
      }
    }

    stage('run2') {
      steps {
        sh 'mvn verify clean test'
      }
    }

    stage('checkout3') {
      steps {
        git(url: 'https://github.com/LakshmiVinoj/maven-samples-A6.git', branch: 'master')
      }
    }

  }
  tools {
    maven 'maven_var'
    jdk 'java_var'
  }
}
