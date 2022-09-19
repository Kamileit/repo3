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
                            script {
                            def dockerCmd = 'docker run -d kmaludzi/docker-node-hello:1.0'
                            sshagent(['ec2-key']) {
                              sh "ssh ec2-user@54.88.229.139 ${dockerCmd}"

                            }
                        }
                    }
                }
            }
        }
    

