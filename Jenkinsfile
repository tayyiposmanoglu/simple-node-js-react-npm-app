pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
        git 'https://github.com/tayyiposmanoglu/simple-node-js-react-npm-app'
      }
    }
     
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
