pipeline {
  agent any 
  
  stages {
    
    stage('Build') {
      steps {
        echo('budujemy')
      }
    }
        
    stage('Test') {
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
        echo 'sukces'
      }
      
      failure {
        echo 'fail'
      }
    }
  
  }
}
