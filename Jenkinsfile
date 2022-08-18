pipeline {
  agent any 
  
  stages {
    
    stage('Build') {
      steps {
        echo(env.BRANCH_NAME)
      }
    }
        
    stage('Test') {
      
      when {
        expression {
          
          env.BRANCH_NAME == "main"
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
