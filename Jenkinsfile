pipeline {
  agent any
    stages {
      stage('Build') {
        steps {
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
          docker run -d -p 8090:80 50000:50000 nginx:alpine
        }

     }
      
   }
}
