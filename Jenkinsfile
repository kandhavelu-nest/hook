pipeline {
agent any
    stages {
        stage('git') {
                         steps {
        git url:'git@github.com:kandhavelu-nest/hook.git', branch:"${BRANCH_NAME}", credentialsId: 'web-app-ssh-key'
      }
        }
    }
    stages {
        stage('Test') {
                         steps {
        sh """
        ls -la
        """
      }
        }
    }
}
