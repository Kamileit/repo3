pipeline {
  agent any 
  parameters{
  
  }
  
  tools {
    
  }
  
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
      //withCredentials([usernamePassword(credentialsId: 'git', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')])
      //when {
        //expression {
          //USERNAME == 'kamilmaludzinski@gmail.com'
        //}
      //}
      
      
      steps {
        echo 'testujemy:'
        //echo USERNAME
        //withCredentials([usernamePassword(credentialsId: 'git', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) 
       
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
