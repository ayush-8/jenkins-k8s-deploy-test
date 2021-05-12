pipeline {
  agent any
  parameters {
    booleanParam(name: "isDeploy" , defaultValue: true)
  }
  stages {
  

      
    stage('test'){
      when {
        expression {
          params.isDeploy
        }
      }
      
      steps {
        echo "test"
        sh "kubectl apply -f k8s-deployment.yml --kubeconfig /admin.conf"
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
