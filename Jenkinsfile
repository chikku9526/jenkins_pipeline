pipeline {
  agent { docker { image '3.6.3-jdk-8' } }
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
