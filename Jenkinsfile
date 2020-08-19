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
            		withKubeConfig([credentialsId: 'dc8af005-5efa-45b7-b9ec-caab715764bd']) {
                   sh 'kubectl get all node'
            		}
        		}
      		}
       } 
   }
}
