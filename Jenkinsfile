pipeline {
  agent any
  
  stages {
        stage ('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage ('Docker Build') {
            steps {
                pwsh(script: 'docker images -a')
                pwsh (script: """
                    cd 'BuildingModernCICDPipelineWithJenkins/azure-voting-app-redis'
                    docker images -a
                    docker build -t mytmptest .
                    dcoker images -a
                 """)
            }
        }
    }
 }
