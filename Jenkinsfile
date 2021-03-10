pipeline {
  agent any
  
  stages {
    stage('Build') {
        build job: params.cls, parameters: [
                string(MAKE: params.MAKE, DEPLOY: "params.DEPLOY")
          ]
      }
    
    stage ('Test') {
      steps {
        echo 'testing'
        }
     }
     
    stage ('Deploy') {
      steps {
        echo 'deploying'
        }
      }
    }
  }
