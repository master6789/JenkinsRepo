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
            		withKubeConfig(credentialsId: '6b78785c-ac66-4d3e-9066-5f57f971284d') {
                   sh 'kubectl get nodes'
            		}
        		}
      		}
       } 
   }
}
