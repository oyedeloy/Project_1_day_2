pipeline {
    agent any
    stages {
        stage('apply') {
          environment {
            AWS_ACCESS_KEY_ID = credentials('ACCESS_KEY')
            AWS_SECRET_ACCESS_KEY = credentials('SECRET_KEY')
        }
       steps {
          sh 'ansible-playbook -i inventory ping.yml'
          sh 'ansible-playbook -i inventory load-balancer.yml'
        }
      }
   }
}