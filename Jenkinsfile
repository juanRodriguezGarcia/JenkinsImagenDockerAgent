pipeline {
    agent {
        // docker {
        //     label 'docker-label'
        //     image 'node:14'
        //     args '-v /var/run/docker.sock:/var/run/docker.sock'
        // }
        docker {
            label 'docker-label'
            image 'node:14'
        }
    }

    // environment {
        // AWS_ACCESS_KEY_ID = credentials('aws-access-key-id')
        // AWS_SECRET_ACCESS_KEY = credentials('aws-secret-access-key')
        // S3_BUCKET = 'your-s3-bucket-name'
    // }
 
	//Checkout: Este paso se asegura de que el código del repositorio esté disponible en el workspace de Jenkins.
    stages {
        // stage('Checkout') {
        //     steps {
        //         checkout scm
        //     }
        // }

        stage('Build') {
            steps {
				echo "##################### Compilando el proyecto ################################"
				sh 'pwd'
				sh 'ls -ltr'
                sh 'npm --version'
				sh 'npm install'
                sh 'npm run build'
            }
        }

        stage('Package') {
            steps {
                sh 'tar -czf build.tar.gz build/'
            }
        }

        // stage('Upload to S3') {
            // steps {
                // withAWS(region: 'us-east-1', credentials: 'aws-credentials-id') {
                    // s3Upload(bucket: S3_BUCKET, path: 'build.tar.gz', file: 'build.tar.gz')
                // }
            // }
        // }
    }

    // post {
        // cleanup {
            // deleteDir()
        // }
    // }
}