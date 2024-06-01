pipeline {
       // agent { docker 'timbru31/java-node:latest' }
  environment {
    HOME="C:/Jenkins"
    DOCKER_CREDENTIALS = credentials('docker-login-credentials')
         
  }
    agent {
        docker {
            image 'openjdk:8-jdk-alpine'
            args  '--rm -v C:/Jenkins:/opt -w /opt'
              //args '-v /var/run/docker.sock:/var/run/docker.sock' 
        }
       //    docker {
       //     label 'doker-label'
       //     image 'openjdk:8-jdk-alpine'
       // }
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
