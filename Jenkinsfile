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

    environment {
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
