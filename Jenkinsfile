
pipeline {
agent any
        stages {
       
        stage('Test') {
                  when {
                expression {
		    
                    result = sh (script: "git log -1 | grep '\\[run\\]'", returnStatus: true) 
		    return result
                }
		beforeAgent true
            }
            steps {               
                sh """
		echo "123"
                git log -1 --pretty=%B
                """
            }
        }
    }
}
