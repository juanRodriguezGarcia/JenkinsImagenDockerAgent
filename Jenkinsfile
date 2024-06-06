pipeline {
    //None es cuando se quiere que compile con el nodo principal	
   // agent any
	///home/jenkins/workspace/ProyectosDemo
		agent {
		   node {
		        label 'label-linux'
		
			   
		    }
    		}




    stages {

        stage('Prepare Workspace') {
            steps {
                script {
                    def workspaceDir = "/home/jenkins/agent/workspace/ProyectosDemo"
                    sh """
                        if [ ! -d "$workspaceDir" ]; then
                            mkdir -p "$workspaceDir"
                        fi
                        sudo chown -R jenkins:jenkins "$workspaceDir"
                        sudo chmod -R 755 "$workspaceDir"
                    """
                }
            }
        }

	stage('Checkout Code') {
            steps {
                git url: 'https://github.com/tu-repositorio.git', branch: 'main'
            }
        }
	    
        stage('Build') {

            steps {
                echo 'Compilando el proyecto......'
		echo '########################################################################## (*-*)##############################################################'
	        sh 'node --version'
                // Aquí van los comandos para compilar tu proyecto
            }
        }
        stage('Test') {
            steps {
                echo 'Ejecutando pruebas...'
                // Aquí van los comandos para ejecutar las pruebas
            }
        }
        stage('Deploy') {
            steps {
                echo 'Desplegando el proyecto...'
                // Aquí van los comandos para desplegar tu proyecto
            }
        }
    }
}
