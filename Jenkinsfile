
pipeline {
agent any
        stages {
       
        stage('Test') {
		environment {
                 result = sh (script: "git log -1 --pretty=%B | grep '\\[run\\]'", returnStatus: true) 
                 }
                when {
		    expression { "${CHORE_RELEASE}" == "1" }
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
