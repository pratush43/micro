pipeline {
  agent {
    node{
    label 'micro1'
    } 
  }
    stages {
        stage('Build') {
            steps {
                sh 'dotnet build'
            }
        }
    }
        post {
        always {
            archiveArtifacts artifacts: 'docs/_framework/_bin/*.dll', onlyIfSuccessful: true
    }
    }
}
