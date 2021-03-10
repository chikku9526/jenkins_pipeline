pipeline {
  agent any
  
    stage('Build') {
        build job: params.cls, parameters: [
                string(MAKE: params.MAKE, DEPLOY: "params.DEPLOY")
          ]
      }
    }
