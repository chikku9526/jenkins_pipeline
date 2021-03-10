pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build job: 'testing2', parameters: [
                string(MAKE: params.MAKE, DEPLOY: "params.DEPLOY")
          ]
       echo "hello"
      }
    }
      }
    }
