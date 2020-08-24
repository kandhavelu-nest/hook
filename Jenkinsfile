
pipeline {
agent any
        stages {
       
        stage('Test') {
                  when {
                expression {
		    last_commit_message = "run"
                    return (last_commit_message =~ /(run)/)
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
