pipeline {
agent any
        stage('Run CI?') {
      agent any
      steps {
        script {
          if (sh(script: "git log -2 --pretty=%B | fgrep -ie '[skip ci]' -e '[ci skip]'", returnStatus: true) == 0) {
            currentBuild.result = 'NOT_BUILT'
            error 'Aborting because commit message contains [skip ci]'
          }
        }
      }
    }

    stages {
        stage('Test') {
            steps {
                sleep 2
                sh 'echo 123'
            }
        }
    }
}
