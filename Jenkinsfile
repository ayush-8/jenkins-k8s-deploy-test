pipeline {
  agent none
  parameters {
    booleanParam(name: "IfDeployed" , defaultValue: true)
  }
  

      
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
