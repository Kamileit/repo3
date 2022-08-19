pipeline {
  agent any 
  
  stages {
    
    stage('Build') {
      steps {
        
        echo ('Budujemy !!!!!!!!!!!!!!!!!!!' + BRANCH_NAME)
        sh 'printenv'
      }
    }
        
    stage('Test') {
      
      when {
        expression {
          
          env.BRANCH_NAME == " "
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
