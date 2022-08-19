pipeline {
  agent any 
  
  stages {
    
    stage('Build') {
      steps {
        
        echo ('Budujemy !!!!!!!!!!!!!!!!!!!' + env.BRANCH_NAME)
        sh 'printenv'
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
