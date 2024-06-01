pipeline {
  agent any
         environment {
           HOME="C:/Jenkins"
           DOCKER_CREDENTIALS = credentials('GIThubCredencialesDocker')       
         }

        
        stages {
            stage('build') {
                steps {
                       script {
                           // Iniciar sesión en Docker dentro del agente Docker
                            withCredentials([usernamePassword(credentialsId: 'GIThubCredencialesDocker', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]) {
                            sh "docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD"
                           }
                            sh 'npm --version'
                       }
                }
           }
        }
    }
