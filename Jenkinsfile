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
        withCredentials([usernamePassword(credentialsId: 'amazon', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
        // available as an env variable, but will be masked if you try to print it out any which way
        // note: single quotes prevent Groovy interpolation; expansion is by Bourne Shell, which is what you want
        sh 'echo $PASSWORD'
        // also available as a Groovy variable
        echo USERNAME
        // or inside double quotes for string interpolation
        echo "username is $USERNAME"
    }
       
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
