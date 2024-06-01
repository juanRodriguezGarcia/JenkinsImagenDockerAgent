pipeline {
       // agent { docker 'timbru31/java-node:latest' }

    agent {
        docker {
            image 'timbru31/java-node:latest'
            args '-v C:\\Jenkins\\directorioAgentes:/opt'
        }
    }
        
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
