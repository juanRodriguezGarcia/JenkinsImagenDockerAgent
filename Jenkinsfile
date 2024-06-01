pipeline {
       // agent { docker 'timbru31/java-node:latest' }
  environment {
    HOME="."
  }
    agent {
        docker {
            image 'timbru31/java-node:latest'
            args '-v ${HOME}:/opt'
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
