pipeline {
  agent any
         environment {
           HOME="C:/Jenkins"
           DOCKER_CREDENTIALS = credentials('docker-login-credentials')       
         }

        
        stages {
            stage('build') {
                steps {
                       script {
                           // Iniciar sesión en Docker dentro del agente Docker
                            withCredentials([usernamePassword(credentialsId: 'docker-login-credentials', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]) {
                            sh "docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD"
                           }
                            sh 'npm --version'
                       }
                }
           }
        }
    }
