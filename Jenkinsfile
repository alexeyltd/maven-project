pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        echo 'init'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
      post {
        success {
          echo 'Archivating'
          archiveArtifacts artifacts: '**/*.war'
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}
