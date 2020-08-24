pipeline {
agent any
    stages {
        stage('Run CI?') {
      agent any
      steps {
        script {
          sh """ git log """ 
        }
      }
    }
        stage('Test') {
            steps {
                sleep 2
                sh 'echo 123'
            }
        }
    }
}
