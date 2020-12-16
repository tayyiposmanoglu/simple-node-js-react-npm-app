pipeline {
  agent any
    
  tools {nodejs "nodeJS"}
    
  stages {
        stage('Initialize') {
            input {
                message 'Is there any commit that will affect the database?'
                ok 'Do it!'
                parameters {
                    string(name: 'DATABASE CHANGES', defaultValue: 'no', description: "${warningMessage}")
                }
            }
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
    
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm run build'
      }
      post {
        success {
            echo "Build completed"
        }
      }
    }  
    
            
    stage('Deliver') {
      steps {
        sh '''
            ls target
         '''
      }
    }
  }
}
