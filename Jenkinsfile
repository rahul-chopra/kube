pipeline {
    agent any
    environment {
        PROJECT_ID = 'forward-emitter-395618'
        CLUSTER_NAME = 'autopilot-cluster-1'
        LOCATION = 'us-east1'
        CREDENTIALS_ID = 'SECRET_TOKEN'
    }
stage('Deploy to GKE') {
            steps{
                sh "sed -i 's/hello:latest/hello:${env.BUILD_ID}/g' dep1.yaml"
                step([$class: 'KubernetesEngineBuilder', projectId: env.PROJECT_ID, clusterName: env.CLUSTER_NAME, location: env.LOCATION, manifestPattern: 'dep1.yaml', credentialsId: env.CREDENTIALS_ID, verifyDeployments: true])
            }
        }
    }    
}
