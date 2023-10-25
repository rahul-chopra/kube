pipeline {

  agent {

    kubernetes {

      label 'my-kubernetes-agent'

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
