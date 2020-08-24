
pipeline {
agent any
        stages {
       
        stage('Test') {
            steps {
                    
                ciSkip action: 'check'
                
                sh """echo 123
                git log -1 --pretty=%B
                """
            }
        }
    }
}
