
pipeline {
agent any
        stages {
       
        stage('Test') {
		environment {
                 result = sh (script: "git log -1 --pretty=%B|grep '.*\\[run\\].*'",returnStatus: true)
	         GIT_COMMIT_MSG = sh (script: 'git log -1 --pretty=%B', returnStdout: true).trim().contains('run')
                 }
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
