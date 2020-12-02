pipeline {
  agent any
  
  stages {
        stage ('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage 'Docker Build') {
            steps {
                pwsh(script: 'docker images -a')
                pwsh (script: """
                    cd "C:\MyDev_DevOps\BuildingModernCICDPipelineWithJenkins\azure-voting-app-redis\azure-vote"
                    docker images -a
                    docker build -t mytmptest .
                    dcoker images -a
                 """)
            }
        }
    }
 }
