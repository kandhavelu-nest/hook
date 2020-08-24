
pipeline {
agent any
        stages {
       
        stage('Test') {
                  when {
                expression {
                    commit_message="run"
                    return (commit_message  =~ /(run)/)
                }
		beforeAgent true
            }
            steps {
                    
           
                
                sh """echo 123
                git log -1 --pretty=%B
                """
            }
        }
    }
}
