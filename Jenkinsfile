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
                sshagent(['ec2']) {
                  sh 'ssh -o StrictHostKeyChecking=no -l  ec2-user 18.212.70.143 uname -a'
                 
                }
            }
        }
    }
}
