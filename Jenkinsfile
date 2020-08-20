pipeline {
  agent any
    stages {
      stage('Build') {
        steps {
          checkout scm
          echo "Building ...."
        }
      }  
      
      stage('Testing') {
        steps {
          echo "Testing ....."
        }
      } 
            
      stage('Deploying') {
        steps {
          echo "Deploying.."
        }

     }
      stage('Apply Kubernetes files') {	
      		steps {
      		  script {
            		withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'minikube', contextName: 'minikube', credentialsId: '6b78785c-ac66-4d3e-9066-5f57f971284d', namespace: 'default', serverUrl: 'https://192.168.99.126:8443']]) {
                   sh 'kubectl get nodes'
                  }
        		}
      		}
       } 
   }
}
