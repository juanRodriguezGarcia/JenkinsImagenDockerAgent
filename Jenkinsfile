pipeline {
  agent any
         environment {
           HOME="C:/Jenkins"
         }

        agent {
        docker { image 'node:20.11.1-alpine3.19' }
    }
  
        stages {
            stage('build') {
                steps {
                       script {
                           // Iniciar sesión en Docker dentro del agente Docker
                             echo "###################### Antes de compilar ####################" 
                             sh 'npm --version'
                           }
                            
                       }
                }
           }
    }
