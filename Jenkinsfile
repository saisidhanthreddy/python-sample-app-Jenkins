@Library('jenkins-shared-library@main') _

buildAndDeploy([
    language: 'python',
    appName: 'my-app',
    environment: 'dev',
    localRegistry: 'localhost:5001',  // Optional: defaults to 'localhost:5000'
    dockerfile: 'Dockerfile',  // Custom Dockerfile path in your repo
    hostPort: 8080,  // Optional: port to expose on host
    containerPort: 8080,  // Custom Dockerfile path in your repo
])

