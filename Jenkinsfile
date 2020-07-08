pipeline {

    agent any

    environment {
        NODE_IMAGE = 'node:12.13.0'
        NODE_IMAGE_ARGS = '-u 0:0'
    }    

    stages {

        stage('Yarn Install') {

            agent {
                docker {
                    image "${env.NODE_IMAGE}"
                    args "${env.NODE_IMAGE_ARGS}"
                }
            }

            steps {
                echo 'Yarn Install'
                echo '******************************'  
                sh 'node --version'
                sh 'yarn --version'
            }
        }
    }    
}
