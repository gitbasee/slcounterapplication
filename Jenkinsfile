pipeline {
  agent any
  stages {
    stage('GetCode') {
      steps {
        git(url: 'https://github.com/gitbasee/simpleMavenJunit.git', branch: 'master', poll: true)
      }
    }

    stage('CompiletheCode') {
      steps {
        sh '''mvn clean
mvn install'''
      }
    }

    stage('packageit') {
      steps {
        sh 'mvn package'
      }
    }

  }
}