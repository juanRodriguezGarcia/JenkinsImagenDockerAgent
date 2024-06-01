pipeline {
       // agent { docker 'timbru31/java-node:latest' }
  environment {
    HOME="C:/Jenkins"
  }
    agent {
        docker {
            image 'node:14'
            args '-w C:/Jenkins'
               
        }
    }
        
        stages {
            stage('build') {
                steps {
                    sh 'npm --version'
                }
           }
        }
    }
