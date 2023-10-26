pipeline {
  agent {
    kubernetes {   
    }
  }

  stages {   
    stage('Deploy to Kubernetes') {
      steps {
         kubernetesDeploy(
          configs: 'kube/dep1.yaml',
          )
      }
    }
  }
}
