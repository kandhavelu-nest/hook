
pipeline {
agent any
        stages {
       
        stage('Test') {
            steps {
                    
                sleep 2
                
                sh """echo 123
                git log -1 --pretty=%B
                """
            }
        }
    }
}
