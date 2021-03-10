pipeline {
  agent { docker { image 'maven:3.3.3' } }
  stages {
    stage('Build') {
      steps {
        build job: params.cls, parameters: [
                string(MAKE: params.MAKE, DEPLOY: "params.DEPLOY")
          ]
       echo "hello"
      }
    }
      }
    }
