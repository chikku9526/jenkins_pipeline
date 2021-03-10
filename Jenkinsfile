pipeline {
  agent { docker { image 'maven' } }
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
