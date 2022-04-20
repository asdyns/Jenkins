pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh "javac HelloWorld.java" 
      }
    }
    stage('test') {
      steps {
        sh "java HelloWorld"
      }
    }
    stage('package') {
      steps {
        archiveArtifacts artifacts: 'HelloWorld.class', followSymlinks: false
      }
    }
  }
}
