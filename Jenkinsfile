pipeline {
    agent any 
    environment {
        PROJECT_ID = 'devopsproject-001'
        CLUSTER_NAME = 'prod'
        LOCATION = 'us-central1-f'
        CREDENTIALS_ID = 'devopsproject-001'
        
        
    }
    stages {
        stage('Deploy to GKE') {
            steps{
                step([$class: 'KubernetesEngineBuilder', projectId: env.PROJECT_ID, clusterName: env.CLUSTER_NAME, location: env.LOCATION, manifestPattern: 'workload.yaml', credentialsId: env.CREDENTIALS_ID, verifyDeployments: true])
            }
        }
    }
}
