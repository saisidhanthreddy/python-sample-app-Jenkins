@Library('jenkins-shared-library@main') _

pipeline {
    agent any
    
    triggers {
        githubPush()
    }
    
    stages {
        stage('Build and Deploy') {
            steps {
                // Example: Using a custom Dockerfile from your app repository
                buildAndDeploy([
                language: 'python',
                appName: 'my-app',
                environment: 'dev',
                localRegistry: 'localhost:5001',  // Optional: defaults to 'localhost:5000'
                dockerfile: 'docker/Dockerfile.prod',  // Custom Dockerfile path in your repo
                hostPort: 8080,  // Optional: port to expose on host
                containerPort: 8080,  // Custom Dockerfile path in your repo
                ])
            }
        }
    }
}





