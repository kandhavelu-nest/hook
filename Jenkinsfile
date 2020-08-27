
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
                 git url:'git@github.com:kandhavelu-nest/hook.git', branch:"${BRANCH_NAME}", credentialsId: 'web-app-ssh-key'            
                sh """
                echo \$BRANCH_NAME
		echo "1234567891011121314151617181920212223242526"
                """
            } 
        }
    }
}
