pipeline {
        agent { docker 'timbru31/java-node:latest' }
        stages {
            stage('build') {
                environment {
                  HOME="."
                }
                steps {
                    sh 'npm --version'
                }
           }
        }
    }
