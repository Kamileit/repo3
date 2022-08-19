pipeline {
  agent any 
  
  environment {
   NEW_VERSION ='1.3.0'
   SERVER_CREDENTIALS = credentials('git')
  }
  
  stages {
    
    stage('Build') {
      steps {
        
        echo ('Budujemy !!!!!!!!!!!!!!!!!!!' + env.BRANCH_NAME)
        echo (env.NEW_VERSION)
      }
    }
    
    stage('env') {
      steps {
       echo (env.BRANCH_NAME)    
      }        
    } 
          
    stage('Test') {
      
      when {
        expression {
          
          env.BRANCH_NAME == "main"
          
        }
      }
      steps {
        echo 'testujemy:'
       
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
