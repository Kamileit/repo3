pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Hello World'
            }
        }
        
        stage('deploy') {
            steps {
                sshagent(['ec2-key']) {
                  sh 'ssh -t -o StrictHostKeyChecking=no ec2-user@54.88.229.139 uname -a'
                  
                }
            }
        }
    }
}
