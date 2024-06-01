pipeline {
  agent any
         environment {
           HOME="C:/Jenkins"
         }

        
        stages {
            stage('build') {
                steps {
                       script {
                           // Iniciar sesión en Docker dentro del agente Docker
                              sh 'npm --version'
                           }
                            
                       }
                }
           }
        }
    }
