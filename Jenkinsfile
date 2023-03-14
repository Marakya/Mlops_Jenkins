pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('run') {
      steps {
        build job: 'requirements.py'
      }
    }
    stage('data creation') {
      steps {
        sh 'python3 data_creation.py'
        echo 'Done'
      }
    }
  }
}
