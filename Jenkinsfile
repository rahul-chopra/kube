pipeline {
    agent any 
    environment {
        PROJECT_ID = 'forward-emitter-395618'
        CLUSTER_NAME = 'autopilot-cluster-1'
        LOCATION = 'us-east1'
        CREDENTIALS_ID = 'SECRET_TOKEN'
    }
    stages {
stage('Build') {
            steps{
                script {
                      kubernetesDeploy(configs: "dep1.yaml")
                }
                
            }
        }
    }   
}
