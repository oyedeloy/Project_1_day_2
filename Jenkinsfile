pipeline {
    agent any
    stages {
        stage('export credentials') {
          environment {
            AWS_ACCESS_KEY_ID = credentials('ACCESS_KEY')
            AWS_SECRET_ACCESS_KEY = credentials('SECRET_KEY')
        }
        stage('build webserver') {
           steps {
                   ansiblePlaybook(
                    credentialsId: 'ssh_auth',
                    inventory: 'inventory',
                    playbook: 'load-balancer.yml'
                 )
              
           }
        }
     }
       
       
       
       