pipeline {
 agent {
  label 'agent'
 }
  stages {
    stage('Build'){
     agent {
        docker { 
         image 'node:18-alpine3.14' 
         reuseNode true}
      }
     steps {
      sh 'node --version'
     }
     }
   stage('Maven'){
    agent {
     docker { 
        image 'maven:3.8.5-jdk-11' 
        reuseNode true
     }
    }
     steps {
        sh 'mvn --version'
     }
   }
  }
}
