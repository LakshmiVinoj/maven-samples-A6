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
        sh 'git checkout 198644632661c67b6c32f59e9047c11a70685e15'
        sh 'mvn verify clean test'
        sh 'git checkout 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
        sh 'mvn verify clean test'
        sh 'git checkout master'
        sh 'git bisect start'
        sh 'git bisect good 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
        sh 'git bisect bad 198644632661c67b6c32f59e9047c11a70685e15'
        sh 'mvn verify clean test'
        sh 'git bisect bad 8bad1c6db9cf6930abd8e52ff5dfdd046194ae9b'
        sh 'mvn verify clean test'
        sh 'git bisect bad 26438de182f7a00147b5e53e9408a3c3745ca509'
        sh 'mvn verify clean test'
        sh 'git bisect reset'
      }
    }
  }
  tools {
    maven 'maven_var'
    jdk 'java_var'
  }
}
