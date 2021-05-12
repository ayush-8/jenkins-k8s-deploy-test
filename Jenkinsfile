pipeline {
  agent any
  parameters {
    booleanParam(name: "IfDeployed" , defaultValue: true)
  }
  stages {
  

      
    stage('test'){
      when {
        expression {
          params.IfDeployed
        }
      }
      
      steps {
        echo "test"
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"
      }
    }
  }
}
