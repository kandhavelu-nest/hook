
pipeline {
agent any
        stages {
       
        stage('Test') {
		environment {
                 result = sh (script: "git log -1 --pretty=%B|grep '.*\\[run\\].*'",returnStatus: true)
	         env.GIT_COMMIT_MSG = sh (script: 'git log -1 --pretty=%B', returnStdout: true).trim()
                 }
               
            steps {               
                sh """
		echo $result
		echo $GIT_COMMIT_MSG
		echo "123"
                git log -1 --pretty=%B
		git log -1 --pretty=%B|grep '.*\\[run\\].*'
                """
            }
        }
    }
}
