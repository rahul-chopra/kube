pipeline {
  agent {
    kubernetes {   
    }
  }

  stages {   
    stage('Checkout Source') {
      steps {
        git 'https://github.com/rahul-chopra/kube'
      }
    }
    stage('Deploy to Kubernetes') {
      steps {
         kubernetesDeploy(
          configs: 'kube/dep1.yaml',
          kubeconfigID: 'secret_token_jenkin_k8'
          )
      }
    }
  }
}
