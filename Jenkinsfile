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
      
   }
}
