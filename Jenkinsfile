pipeline {
  agent any
    
  tools {nodejs "nodeJS"}
    
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
