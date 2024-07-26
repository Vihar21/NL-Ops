pipeline {
    agent any

    stages {
}	
        stage('Build') {
            steps {
                script {
                    // Use Windows batch command to install dependencies
                    bat 'pip install -r requirements.txt'
                }
            }
        }
        stage('Docker Build') {
            steps {
                script {
                    // Use Windows batch command to build Docker image
                    bat 'docker build .'
                }
            }
        }

    }
}
    

    post {
        always {
            cleanWs()
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs for details.'
        }
    }
}