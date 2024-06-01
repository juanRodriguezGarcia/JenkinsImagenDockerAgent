pipeline {
       // agent { docker 'timbru31/java-node:latest' }
  environment {
    HOME="C:/Jenkins"
    DOCKER_CREDENTIALS = credentials('docker-login-credentials')
         
  }
    agent {
        docker {
            image 'node'
            //args '-v C:/Jenkins:/opt -w /opt'
              args '-v /var/run/docker.sock:/var/run/docker.sock' 
        }
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
