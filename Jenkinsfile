pipeline {
agent any
    stages {
        stage('Test') {
                         steps {
        git url:'git@github.com:kandhavelu-nest/hook.git', branch:"${BRANCH_NAME}", credentialsId: 'web-app-ssh-key'
      }
        }
    }
}
