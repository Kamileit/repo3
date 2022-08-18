pipeline {
  agent any 
  
  stages {
    
    stage('Build') {
      steps {
        echo('budujemy')
      }
    }
        
    stage('Test') {
      
      when {
        expression {
          
          BRANCH_NAME == "dev" || BRANCH_NAME == "main"
        }
      }
        steps {
          echo ('testujemy')
        
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
