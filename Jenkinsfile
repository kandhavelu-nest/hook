
pipeline {
agent any
        stages {
       
        stage('Test') {
                  when {
                expression {
                    commit_message="run"
                    return (git log -1 --pretty=%B =~ /(run)/)
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
