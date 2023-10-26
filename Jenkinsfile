pipeline {
  agent {
    kubernetes {   
    }
  }

  stages {   
    stage('Deploy to Kubernetes') {
      steps {
        script {
        kubernetesDeploy(
          configs: 'kube/dep1.yaml',
          )
      }
      }
    }
  }
}
