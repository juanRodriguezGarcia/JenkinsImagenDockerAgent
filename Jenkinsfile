pipeline {
    agent {
        label 'label-linux'
    }
    stages {
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
