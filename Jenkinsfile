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
                  sh 'cat /var/jenkins_home/workspace/pipepline@tmp/private_key*'
                 
                }
            }
        }
    }
}
