pipeline {
 agent any
  stages {
    stage('Build'){
     agent {
        docker { image 'node:18-alpine3.14' }
      }
     steps {
      sh 'node --version'
     }
     }
   stage('Maven'){
    agent {
     docker { image maven:3.8.5-jdk-11' }
    }
     steps {
        sh 'mvn --version'
     }
   }
  }
}
