
pipeline {
agent any
        stages {
       
        stage('Test') {
		environment {
                 result = sh (script: "git log -1 --pretty=%B")
                 }
                
            steps {               
                sh """
		echo $result
		echo "123"
                git log -1 --pretty=%B
                """
            }
        }
    }
}
