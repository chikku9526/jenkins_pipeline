pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build job: "https://2886795295-8080-cykoria03.environments.katacoda.com/job/testing2/", parameters: [
                string(MAKE: params.MAKE, DEPLOY: "params.DEPLOY")
          ]
       echo "hello"
      }
    }
      }
    }
