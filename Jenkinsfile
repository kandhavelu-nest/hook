
pipeline {
agent any
        stages {
       
        stage('Test') {
                  when {
                expression {
		    last_commit_message = sh(script: 'git log -1 --pretty=%B')
		    sh (script: 'echo $last_commit_message')
                    return   sh(script: 'git log -1 --pretty=%B')
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
