pipeline {
  agent any 

  stages {
    
    
    stage('Build') {
      
      
      steps {
        
        echo ('Budujemy !!!!!!!!!!!!!!!!!!!' + env.BRANCH_NAME)
        echo (env.NEW_VERSION)
        
        
      }
    }
    
    stage('env') {
      steps {
       
      }        
    } 
          
    stage('Test') {
      
      
      
      
      steps {
        echo 'testujemy bool:'
         
         
       
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
}
