pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo "Compiling..."
        sh "javac HelloWorld.java" 
      }
    }
    stage('test') {
      steps {
        echo "Building..."
        sh "java HelloWorld"
      }
    }
    stage('package') {
      steps {
        echo "Archiving..."
        archiveArtifacts artifacts: 'HelloWorld.class', followSymlinks: false
      }
    }
  }
}
