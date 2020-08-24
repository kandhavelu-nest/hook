
pipeline {
agent any
        stages {
       
        stage('Test') {
		
		when {
                expression {
                   return sh (script: 'git log -1 --pretty=%B', returnStdout: true).trim().contains('run')
                }
		beforeAgent true
            }
               
            steps {               
                sh """
		echo $result
		echo $GIT_COMMIT_MSG
                """
            }
        }
    }
}
