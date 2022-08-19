pipeline {
  agent any 
  parameters{
  choice (name: 'VERSION', choices: [1,2,3],description:' ')
  booleanParam (name: "test" ,defaultValue: true)
  booleanParam (name: "test" ,defaultValue: inne)

          
  }
  
  tools {
    maven 'maven 3.8.6'
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
      when {
        expression {
           params.test == true
        }
      }
      
      
      steps {
        echo 'testujemy bool:'
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
