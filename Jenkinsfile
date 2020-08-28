
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
		echo "12345678910111213141516171819202122232425262728293031"
                """
                hangoutsNotify message: "This message is from a pipeline!",token: "e-1gx-GTeu6d3_98z0CBwdWjq",threadByJob: true
            } 
        }
    }
}
