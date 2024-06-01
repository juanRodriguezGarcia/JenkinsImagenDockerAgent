pipeline {
agent any
//agent { dockerfile true }	 


	







	
	
	stages {		
        stage('build') {



		
            steps {
                script {

						docker.withServer('tcp://localhost:2375') {
							docker.image('node:20.11.1-alpine3.19').inside {
								sh 'npm --version'
							}
						}

			
						   /* the return value gets caught and saved into the variable MY_CONTAINER */
						   MY_CONTAINER = bat(script: '@docker run -d -i python:3.10.7-alpine', returnStdout: true).trim()
							
							echo "mycontainer_id is ${MY_CONTAINER}"
						   /* python --version gets executed inside the Container */
						   bat "docker exec ${MY_CONTAINER} python --version "
						   /* the Container gets removed */
						   bat "docker rm -f ${MY_CONTAINER}"
                        }
                    }
                }
            }
        }
