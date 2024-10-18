pipeline {
    agent any

    environment {
        DOCKER_CREDENTIALS = credentials('docker credentials') // Your Docker Hub credentials
        KUBECONFIG = credentials('kubeconfig') // Your Minikube kubeconfig
    }

    stages {
         stage('DockerHub Login') {
            steps {
                script {
                    sh '''
                        echo $DOCKER_CREDENTIALS_PSW | docker login -u $DOCKER_CREDENTIALS_USR --password-stdin
                    '''
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                sh '''
                    echo "Building Docker image..."
                    docker build -t ahmed862/simple-app1 .
                '''
            }
        }

        stage('Push Docker Image') {
            steps {
                sh '''
                    docker push ahmed862/simple-app1
                '''
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                        echo "Deploying to namespace..."
                        
                         sh 'kubectl apply -f testdeploy.yaml '
                        
                }
            
        }
    }

    post {
        success {
            echo "Deployment to successful!"
        }
        failure {
            echo "Deployment to failed!"
        }
    }
}
