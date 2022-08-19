pipeline {
  agent any 
  
  stages {
    
    stage('Build') {
      steps {
        
        echo ('Budujemy !!!!!!!!!!!!!!!!!!!')
        sh 'printenv'
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
      
      stage('Build') {
        steps {
          echo 'Pulling...' + env.BRANCH_NAME
          checkout scm
        
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
