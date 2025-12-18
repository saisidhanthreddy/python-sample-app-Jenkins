@Library('jenkins-shared-library') _

// Example: Using a custom Dockerfile from your app repository
buildAndDeploy([
    language: 'python',
    appName: 'my-app',
    environment: 'prod',
    ecrRegistry: '123456789012.dkr.ecr.us-east-1.amazonaws.com',
    clusterName: 'prod-eks-cluster',
    awsRegion: 'us-east-1',
    dockerfile: 'Dockerfile'  // Custom Dockerfile path in your repo
])

