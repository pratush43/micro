pipeline {
  agent {
      	docker {
        	image 'pratush43/sdk:latest'
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
