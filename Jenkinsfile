pipeline {
  agent none
  stages {
    stage('test'){
      steps {
        echo "test"
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"
      }
    }
  }
}
