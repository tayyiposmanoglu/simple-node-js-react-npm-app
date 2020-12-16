pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        

     
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm run build'
      }
    }  
    
            
    stage('Deliver') {
      steps {
        echo "Deliver"
      }
    }
  }
}
