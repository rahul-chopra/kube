pipeline {
  agent {
    kubernetes {   
    }
  }

  stages {   
    stage('Deploy to Kubernetes') {
      steps {
        kubernetesDeploy(
          configs: 'kubernetes/dep1.yaml',
          kubeconfigId: 'my-kubeconfig'
        )
      }
    }
  }
}
