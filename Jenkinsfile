pipeline {
  agent {
      	docker {
        	image 'bitnami/aspnet-core'
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
