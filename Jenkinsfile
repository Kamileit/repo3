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
       echo (env.SERVER_CREDENTIALS)
      }        
    } 
          
    stage('Test') {
      steps {
        echo 'testujemy:'
        withCredentials ([
          usernamePassword(credentials: 'git', usernameVariable: USER, passwordVariable:PWD)
          ])
       
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
