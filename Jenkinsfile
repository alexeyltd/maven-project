pipeline {
  agent any
  stages {
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
  }
}
