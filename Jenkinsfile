pipeline {
    agent any
    stages {
        stage('apply') {
          environment {
            AWS_ACCESS_KEY_ID = credentials('ACCESS_KEY')
            AWS_SECRET_ACCESS_KEY = credentials('SECRET_KEY')
        }
       steps {
          sh 'ansible -m ping -i inventory redis_nodes'        
        }
      }
   }
}