
pipeline {
agent any
        stages {
       
        stage('Test') {
		environment {
			env.CI_SKIP="false"
                 result = sh (script: "git log -1 --pretty=%B|grep '.*\\[run\\].*'",returnStatus: true)
			if (result == 0) {
                        env.CI_SKIP = "true"
			}
			echo $CI_SKIP
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
