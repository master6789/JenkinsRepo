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
            		withKubeConfig(credentialsId: '416c1ee7-679b-4b23-bbb4-8ca6071e5a98') {
                   sh 'kubectl get all node'
            		}
        		}
      		}
       } 
   }
}
