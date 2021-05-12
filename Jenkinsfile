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
  post {
    success {
      echo "Successful Deployment"
    }
    failure {
      echo "Failed Deployment"
    }
    always {
      echo "Be Patient"
    }
  }
  
}
