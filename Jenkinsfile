pipeline {
  agent any

  stages {   
    stage('Checkout Source') {
      steps {
        git 'https://github.com/rahul-chopra/kube.git'
      }
    }
    stage('Deploy to Kubernetes') {
      steps {
        script {
         kubernetesDeploy(configs: "dep1.yaml")
          }
      }
    }
  }
}
