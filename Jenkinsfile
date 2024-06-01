pipeline {
       // agent { docker 'timbru31/java-node:latest' }
  environment {
    HOME="C:/Jenkins"
  }
    agent {
        docker {
            image 'node'
            args 'v C:/Jenkins:/opt -w /opt'
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
