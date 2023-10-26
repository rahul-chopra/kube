pipeline {
  agent {
    kubernetes {   
    }
  }

  stages {   
    stage('Deploy to Kubernetes') {
      steps {
        scritr {
        kubernetesDeploy(
          configs: 'kube/dep1.yaml',
          kubeconfigId: 'my-kubeconfig'
        )
      }
      }
    }
  }
}
