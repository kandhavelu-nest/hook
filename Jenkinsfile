
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
		echo "123456789101112131415161718"
                """
            }
		 stage("preserve build user") {
            wrap([$class: 'BuildUser']) {
                GET_BUILD_USER = sh ( script: 'echo "${BUILD_USER}"', returnStdout: true).trim()
            }
        }
        }
    }
}
