pipeline {
  agent any 
  
  stages {
    
    stage('Build') {
      steps {
        
        echo ('Budujemy !!!!!!!!!!!!!!!!!!!')
        sh 'printenv'
      }
    }
        
    stage('Test') {
      
      when {
        expression {
          
          env.BRANCH_NAME == "main"
        }
      }
        steps {
          echo 'testujemy:' env.BRANCH_NAME
        
      }
    }
  }
    
    
  post {
      
      always { 
        echo 'zawsze'
      }

      success {
        echo 'sukces !!!!!!!!!!!!!!!!!!!!!1'
      }
      
      failure {
        echo 'fail'
      }
    }
  }
